<template>
  <div id="app">
    
    <link rel="stylesheet" href="@/assets/projects/projects.css" type="text/css">

    <Header />
    <div class="main">
      <transition name="fade" mode="out-in">
        <router-view/>
      </transition>
    </div>
    <Footer />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Helpers from './helpers';

export default Vue.extend({
  name: 'App',
  components: {
    Header, Footer
  }
});

// Preload heavy images or gifs that are used in other pages
Helpers.preloadImages([
"img/projects/games/bladehit.gif",
  "img/projects/games/blokndino.gif",
  "img/projects/games/crazyspace.gif",
  "img/projects/games/dancemonkey.gif",
  "img/projects/games/dodge.gif",
  "img/projects/games/eaglesquadron.gif",
  "img/projects/games/keells.gif",
  "img/projects/games/mandapama.gif",
  "img/projects/games/nerotarget.gif",
  "img/projects/games/royalblade.gif",
  "img/projects/games/shhuriken.gif",

  "img/projects/screenshots/keells_menu.png",
  "img/projects/screenshots/shuriken_menu.png",
  "img/projects/screenshots/nero_game.png",
  "img/projects/screenshots/blokndino_ad.jpg",
  "img/projects/screenshots/eagle_menu.png",
  "img/projects/screenshots/r_blade_menu.png",
  "img/projects/screenshots/bladehit_menu.png",
  "img/projects/screenshots/dodge_menu.png",
  "img/projects/screenshots/crazyspace_menu.png",

  "img/projects/toolProjects/imitemplate.png",
  "img/projects/toolProjects/secuityThumb.jpg",

  "img/projects/screenshots/hiveMenu.jpg",
  "img/projects/screenshots/ar_1.jpeg",
  "img/projects/other/tutorials.jpg",
  "img/projects/other/blogs.jpg",

  "img/projects/screenshots/kanthi_menu.png",
  "img/projects/screenshots/heena_perata_menu.png",
  "img/projects/screenshots/dncemonkey_menu.png",
  "img/projects/screenshots/manda_pama_menu.png",

  "img/projects/other/neospic2.jpg",
  "img/projects/other/election.jpg",
]);

</script>

<style lang="less">

@import './css/projects.less';
@import './css/variables.less';

html, body {
  margin: 0px;
  background-color: @bodyBgColor;
}

body {
  -ms-overflow-style: none; /* for Internet Explorer, Edge */
  scrollbar-width: none; /* for Firefox */
  overflow-y: scroll; 
}

body::-webkit-scrollbar {
  display: none; /* for Chrome, Safari, and Opera */
}

#app {
  background-color: @contentBgColor;
  color: @textColor;

  font-family: 'Karla', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  font-size: 1.1em;
  line-height: 1.6em;
  text-align: justify;
}

h1, h2, h3, h4, h5 {
  text-align: left;
}

a {
  color: @textColor;
  text-decoration: none;
  opacity: 0.5;
}
a:hover, .router-link-exact-active {
  opacity: 1;
}

h1 {
  font-size: 2.5em;
  font-weight: 100;
  margin-top: -10px;
  margin-bottom: 40px;
  margin-left: -2px; // hack to make it "seem" more aligned with smaller text content
  line-height: 1.1em;
}

.main {
    padding: 12px;
  }

@media only screen and (min-width: 620px){

  #app {
    text-align: left;
    line-height: 1.8em;
  }

  h1 {
    margin-top: 0.67em;
    margin-bottom: 80px;
    line-height: 0.7em;
  }

  .main {
    padding: 0px 40px 40px 180px;
  }

  .main, .header, .footer {
    max-width: 1200px;
    margin: 0 auto;
  }
}

.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.2s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0
}

</style>
