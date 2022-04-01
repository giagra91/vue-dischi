<template>
        <div class="card my-card text-white text-center p-3" >
            <img :src="card.poster" class="card-img-top" alt="">
            <div class="card-body">
                <h5 class="card-title text-uppercase fw-bold">{{ card.title }}</h5>
                <p class="card-text m-0">{{ card.author }}</p>
                <p class="card-text m-0">{{ card.year }}</p>
            </div>
        </div>
        
</template>

<script>
export default {
    name: "AlbumCard",
    props: 
    {
        card : Object,
    }

}
</script>

<style lang="scss" scoped>
@import "../assets/style/partials/variables.scss";

    div.my-card{
        width: calc((100% /5) - 1.6rem);
        min-width: 160px;
        background-color: $BrandColor;
        margin: .3rem .8rem;

        h5{
            font-size: .95rem;
            cursor: pointer;

            &:hover{
                text-decoration: underline;
            }
        }

        p{
            font-size: .8rem;
            color: grey;
}
    }

</style>