<template>
    <div class="text-white">
        <h1>Loading...</h1>
        <div class="loading">

        </div>
    </div>
</template>

<script>
export default {
    name: "LoadingElement",

}
</script>

<style lang="scss" scoped>

    div.loading{
        width: 250px;
        height: 250px;
        background-image: url("../assets/images/logo.svg");
        background-repeat: no-repeat ;
        background-position: center;
        animation: spin 2s linear infinite;
    }

    @keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
    }

</style>