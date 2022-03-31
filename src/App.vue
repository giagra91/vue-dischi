<template>
  <div id="app">
    <Header @search="searchMusicGenre" />

    <main>
      <Main :genreToSearch="genreToSearch" />
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
    }
  },
  components: {
    Header,
    Main
  },
  methods:{
    searchMusicGenre(newWord){
      this.genreToSearch=newWord
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
