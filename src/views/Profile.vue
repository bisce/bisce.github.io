<template>
    <div class="profile">
        <h1>資格</h1>
        <!-- 資格 -->

        <QualificationList />
    </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import QualificationList from "@/components/QualificationList.vue";
@Component({
    components: {
        QualificationList
    }
})
export default class extends Vue {}
</script>

<style lang="scss">
.profile {
    max-width: 720px;
    margin: 0 auto;
    padding: 0 16px;
    > h1 {
        margin: 12px 0 32px;
        font-size: 24px;
        border-left: 4px solid #42b983;
        padding-left: 8px;
    }
    > p {
        margin-top: 8px;
        font-size: 14px;
        letter-spacing: 2px;
    }
}
</style>
