<template>
    <div class="my-header">
        <img class="m-3" src="../assets/images/logo.svg" alt="">
        <div class="my-search m-auto">
            <label class="text-white me-1" for="my-genre">Seleziona genere</label>
            <select @click="$emit(`search`, selectValue)" v-model="selectValue" class="text-center" name="music-genre" id="my-genre">
                <option value="">Nessuna preferenza</option>
                <option value="rock">Rock</option>
                <option value="pop">Pop</option>
                <option value="jazz">Jazz</option>
                <option value="metal">Metal</option>
            </select>
            
            <label class="text-white ms-2 me-1" for="my-author">Seleziona autore</label>
            <select @click="$emit(`searchAuthor`, selectAuthor)" v-model="selectAuthor" class="text-center" name="music-author" id="my-author">
                <option value="">Nessuna preferenza</option>
                <option value="bon jovi">Bon Jovi</option>
                <option value="queen">Queen</option>
                <option value="sting">Sting</option>
                <option value="steve gadd band">Steve Gadd Band</option>
                <option value="iron maiden">Iron Maiden</option>
                <option value="eric clapton">Eric Clapton</option>
                <option value="deep purple">Deep Purple</option>
                <option value="metallica">Metallica</option>
                <option value="dave weckl">Dave Weckl</option>
                <option value="michael jacjson">Michael Jacjson</option>
            </select>

        </div>
    </div>
</template>

<script>
export default {
    name: "IndexHeader",
    data: function(){
        return{
            selectValue: "",
            selectAuthor: "",
        }
    },
    methods: {
    },
}
</script>

<style lang="scss" scoped>
@import "../assets/style/partials/variables.scss";

div.my-header{
    height: 9vh;
    background-color: $BrandColor;
    display: flex;
    align-items: center;

    img{
        height: 55%;
    }

    select{
        width: 200px;
    }
}

</style>