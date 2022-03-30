<template>
  <div id="app">
    <Header />

    <main>
      <Main />
    </main>

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'


export default {
  name: 'App',
  components: {
    Header,
    Main
  }
}
</script>

<style lang="scss">
@import "./assets/style/style.scss";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
