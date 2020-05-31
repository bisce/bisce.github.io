<template>
    <section class="qualification">
        <div class="date">{{date}}</div>
        <div class="name">{{name}}</div>
    </section>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class extends Vue {
    @Prop()
    public date!: string;
    @Prop()
    public name!: string;
}
</script>

<style lang="scss">
.qualification {
    margin: 32px 0;
    .date {
        margin-bottom: 4px;
        font-weight: 700;
    }
}

@media screen and (min-width: 540px) {
    .qualification {
        display: flex;
        .date {
            padding-right: 40px;
        }
    }
}
</style>
