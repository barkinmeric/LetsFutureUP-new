<template>
<div class="depSec">
    <department-desc :secText="secText" />
    <department-img :secImg="secImg"/>
</div>
</template>

<script>
import DepartmentDesc from './sectionComponents/DepartmentDesc.vue'
import DepartmentImg from './sectionComponents/DepartmentImg.vue'
export default {
    components: { DepartmentDesc, DepartmentImg },
    props: ['secData'],
    data() {
        return {
            secText: this.secData.text,
            secImg: this.secData.imgs
        }
    }
}
</script>

<style lang="scss" scope>
    .depSec {
        display: flex;
        justify-content: center;
        align-content: center;
        flex-flow: row wrap;
    }
</style>