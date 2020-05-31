<template>
    <div class="home">
        <div class="title">
            <h1>Portfolio - Kenta Seno</h1>
            <h3>Programmer / Enginer</h3>
        </div>
        <WorkList />
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import WorkList from "@/components/WorkList.vue";
@Component({
    components: {
        WorkList
    }
})
export default class extends Vue {}
</script>

<style lang="scss">
.home {
    display: flex;
    flex-direction: column;
    justify-content: center;
    > .title {
        margin: 24px 0 48px;
        h1 {
            margin: 0;
            margin-top: 12px;
            text-align: center;
            font-size: 24px;
        }
        h3 {
            margin: 0;
            margin-top: 8px;
            text-align: center;
            font-size: 15px;
            color: #999;
        }
    }
    > .image {
        width: 100%;
    }
}
</style>
