<template>
    <div class="my-header">
        <img class="m-3" src="../assets/images/logo.svg" alt="">
    </div>
</template>

<script>
export default {
    name: "IndexHeader",

}
</script>

<style lang="scss" scoped>
@import "../assets/style/partials/variables.scss";

div.my-header{
    height: 9vh;
    background-color: $BrandColor;

    img{
        height: 55%;
        vertical-align: middle;
    }
}

</style>