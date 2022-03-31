<template>
    <div class="my-header">
        <img class="m-3" src="../assets/images/logo.svg" alt="">
        <div class="my-search m-auto">
            <label class="text-white me-1" for="my-select">Seleziona genere</label>
            <select @click="$emit(`search`, selectValue)" v-model="selectValue" class="text-center" name="music-genre" id="my-select">
                <option value="rock">Rock</option>
                <option value="pop">Pop</option>
                <option value="jazz">Jazz</option>
                <option value="metal">Metal</option>
                <option value="">Nessuna preferenza</option>
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
        }
    },
    methods: {
        checkValue() {
            let newValue = this.selectValue
            console.log(newValue)          
        },
        resetValue(){
            this.selectValue="";
        }
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
        width: 150px;
    }
}

</style>