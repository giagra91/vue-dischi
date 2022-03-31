<template>
  <div id="app">
    <Header @search="searchMusicGenre" @searchAuthor="searchNameAuthor"/>

    <main>
      <Main :genreToSearch="genreToSearch" :nameToSearch="nameToSearch"/>
    </main>

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'


export default {
  name: 'App',
  data: function(){
    return{
      genreToSearch:"",
      nameToSearch:"",
    }
  },
  components: {
    Header,
    Main
  },
  methods:{
    searchMusicGenre(newWord){
      this.genreToSearch=newWord
    },
    searchNameAuthor(newName){
      this.nameToSearch=newName
    }
  }
}
</script>

<style lang="scss">
@import "./assets/style/style.scss";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
