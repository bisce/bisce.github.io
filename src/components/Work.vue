<template>
    <article class="work">
        <div class="image" ref="image" :style="{backgroundImage:'url('+ work.image +')'}"></div>
        <div class="info">
            <span class="date">{{work.date}}</span>
            <div class="title">{{work.title}}</div>
            <div class="description">{{work.description}}</div>
        </div>
    </article>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class extends Vue {
    @Prop({ required: true })
    public work!: {
        image: string;
        date: string;
        title: string;
        description: string;
    };

    mounted(): void {
        window.addEventListener("resize", this.setHeight);
        this.setHeight();
    }
    private setHeight(): void {
        if (!(this.$refs.image instanceof HTMLDivElement)) return;
        const element: HTMLDivElement = this.$refs.image;
        element.style.height = this.calcHeight();
    }
    private calcHeight(): string {
        if (!(this.$refs.image instanceof HTMLDivElement)) return "0px";
        const element: HTMLDivElement = this.$refs.image;
        return (element.offsetWidth / 4) * 3 + "px";
    }
}
</script>

<style lang="scss">
.work {
    margin-bottom: 64px;
    width: 100%;
    .image {
        background: center center/cover no-repeat #eee;
    }
    .info {
        padding: 8px 16px 16px;
        .date {
            font-size: 14px;
            color: #999;
        }
        .title {
            font-size: 16px;
            font-weight: 700;
            color: #2c3e50;
            line-height: 24px;
        }
        .description {
            margin-top: 8px;
            line-height: 24px;
        }
    }
    @media screen and (min-width: 540px) {
        margin: 0 20px 32px 20px;
        width: calc((100% / 2) - 40px);
        .image {
            border-radius: 4px;
        }
        .info {
            padding: 8px 1px;
        }
    }
    @media screen and (min-width: 900px) {
        margin: 0 10px 32px 10px;
        width: calc((100% / 3) - 20px);
    }
}
</style>
