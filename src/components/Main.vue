<template>
    <div class="my-products">

        <div class="albums">
        <AlbumCard v-for="(element, index) in newArray" :key="index" :card="element"/>

        </div>
    </div>
</template>

<script>
import axios from "axios";

import AlbumCard from "./AlbumCard.vue"

export default {
    name: "IndexMain",
    data: function(){
        return{
            newArray: [],
        }
    },
    components:{
        AlbumCard
    },
    created: function(){
        this.getApiInfo();
    },
    methods: {
        getApiInfo(){
            axios.get(`https://flynn.boolean.careers/exercises/api/array/music`)
            .then((result) => {
                this.newArray=result.data.response;
            console.log(result.data.response);
            })
            .catch((error) => {
            console.error(error)
            })
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/partials/variables.scss";
    div.my-products{
        background-color: $BgColor;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 3rem 0;

        div.albums{
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            width: 70%;
        }
    }

</style>