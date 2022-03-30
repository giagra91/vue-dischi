<template>
    <div class="my-products">
        <Card />
    </div>
</template>

<script>
import Card from "./Card.vue"

export default {
    name: "IndexMain",
    components:{
        Card
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/partials/variables.scss";
    div.my-products{
        height: 91vh;
        background-color: $BgColor;
    }


</style>