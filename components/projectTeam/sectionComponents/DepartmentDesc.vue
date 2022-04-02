<template>
    <div id="depDesc">
        <h2>{{departmentTitle}}</h2>
        <article>{{departmentDesc}}</article>
    </div>
</template>

<script>
export default {
    props: [ 'secText' ],
    data() {
        return {
            departmentTitle: this.secText.title,
            departmentDesc: this.secText.description
        }
    }
}
</script>

<style lang="scss" scope>
    #depDesc {
        font-style: normal;
        text-align: center;
        letter-spacing: 0.3px;
        width: 50%;
        padding: 20px;
        @media (max-width: 800px) {
            width: 100%;
        }
    }
</style>