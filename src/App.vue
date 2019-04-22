<template>
  <div id="app">
    <header>
      <h1 id="title">The Bowl Shop</h1>
      <img src=".\assets\img\logo.svg" id="logo" alt="logo">

      <div id="tabs">
        <a v-on:click="activetab=1" v-bind:class="[ activetab === 1 ? 'active' : '' ]">Home</a>
        <a v-on:click="activetab=2" v-bind:class="[ activetab === 2 ? 'active' : '' ]">Bowls</a>
        <a v-on:click="activetab=3" v-bind:class="[ activetab === 3 ? 'active' : '' ]">About</a>
      </div>
    </header>

    <div class="content">
      <div v-if="activetab === 1" class="tab-content">
        <transition name="fade">
          <Home v-on:menu-btn="activetab = $event"></Home>
        </transition>
      </div>

      <div v-else-if="activetab === 2" class="tab-content">
        <transition name="fade">
          <Bowls/>
        </transition>
      </div>

      <div v-else-if="activetab === 3" class="tab-content">
        <transition name="fade">
          <About/>
        </transition>
      </div>
     
    </div>
     <Footer/>
  </div>
</template>

<script>
import Bowls from "./components/Bowls.vue";
import Home from "./components/Home.vue";
import About from "./components/About.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Bowls,
    Home,
    About,
    Footer
  },
  data() {
    return {
      activetab: 1
    };
  }
};
</script>
<style lang="scss" >
@import "./assets/style/bowl_shop.scss";
header {
    padding-top:2em;
  //important
  @include h-w(20vh, 100vw);
  position: static;
  text-align: center;
  margin: auto;
  #title {
    @extend %reset;
   
    font-size: 3em;
    display: inline;
  }
  #logo {
    width: 50px;
    @extend %reset;
  }

  #tabs {
    @include flex(flex, row, wrap, center, center);
    @include h-w(5em, 100%);
  }
}
.fade-enter-active {
  transition: opacity 1s;
}
.fade-enter {
  opacity: 0;
}
#content {
  @include h-w(100%, 100%);
  .tab-content {
    @include h-w(100%, 100%);
  }
}
.active {
  text-decoration: underline;
}
</style>

