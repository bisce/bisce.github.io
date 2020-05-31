<template>
    <div class="work-list">
        <Work v-for="item in items" :work="item" :key="item.title"></Work>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import Work from "@/components/Work.vue";

@Component({
    components: {
        Work
    }
})
export default class extends Vue {
    private items = [
        {
            image: require("@/assets/portfolio.png"),
            date: "2020.03",
            title: "Portfolio",
            description: "ポートフォリオを公開するために作成。"
        }
    ];
}
</script>
<style lang="scss">
.work-list {
    display: flex;
    flex-wrap: wrap;
    max-width: 1080px;
    width: 100%;
    margin: 0 auto;
}
</style>