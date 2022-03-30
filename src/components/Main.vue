<template>
    <div class="my-products">

        <div class="albums" v-if="newArray">
            <AlbumCard v-for="(element, index) in newArray" :key="index" :card="element"/>
        </div>

        <div v-else>
            <Loading />
        </div>

    </div>
</template>

<script>
import axios from "axios";

import AlbumCard from "./AlbumCard.vue"
import Loading from './Loading.vue'


export default {
    name: "IndexMain",
    data: function(){
        return{
            newArray: null,
            apiAlbums: "https://flynn.boolean.careers/exercises/api/array/musi",
        }
    },
    components:{
        AlbumCard,
        Loading,
    },
    created: function(){
        setTimeout(this.getApiInfo, 3000, this.apiAlbums)
    },
    methods: {
        getApiInfo(newApi){
            axios.get(newApi)
            .then((result) => {
                this.newArray=result.data.response;
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