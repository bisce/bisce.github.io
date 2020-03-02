<template>
    <div>
        <Qualification v-for="item in items" :key="item.name" :date="item.date" :name="item.name"></Qualification>
    </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Qualification from "@/components/Qualification.vue";
@Component({
    components: {
        Qualification
    }
})
export default class extends Vue {
    private items = [
        {
            date: "2019.10",
            name: "ネットワークスペシャリスト試験"
        },
        {
            date: "2019.08",
            name: "CompTIA Security+"
        },
        {
            date: "2019.04",
            name: "データベーススペシャリスト試験"
        },
        {
            date: "2018.10",
            name: "情報処理安全確保支援士(合格のみ)"
        },
        {
            date: "2018.04",
            name: "応用情報技術者試験"
        },
        {
            date: "2017.10",
            name: "基本情報技術者試験"
        }
    ];
}
</script>


<style lang="scss">

</style>
