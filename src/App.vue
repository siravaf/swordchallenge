<template>
  <div id="app">
    <Header/>
    <Profile/>
    <Game/>
    <Stats/>
    <Footer/>
  </div>
</template>

<script>
    import Header from './components/layouts/Header';
    import Profile from "@/components/layouts/Profile";
    import Game from "@/components/layouts/Game";
    import Footer from "@/components/layouts/Footer";
    import Stats from "@/components/layouts/Stats";
    export default {
        name: 'app',
        components: {
            Header,
            Profile,
            Footer,
            Game,
          Stats
        }
    }
</script>


<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: left;
    color: #2c3e50;
    margin-top:auto;
  }
</style>
