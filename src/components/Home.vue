<template>
  <div id="home">
    <div id="landing-banner" class="banner">
      <h2>Hearty Bowls, On the Go</h2>

      <h3>
        <a v-on:click="$emit('menu-btn',2)">Menu</a>
      </h3>
    </div>
    <div id="promo">
      <div id="promo-left" class="banner">
        <h2>New at The Bowl Shop, our dumpling soup, made fresh daily.</h2>
        <h3>
          <a v-on:click="$emit('menu-btn',2)">Check it out</a>
        </h3>
      </div>
      <div id="promo-right" class="banner">
        <h2>Not down with meat? Come and see how we "Buddha" our bowls!</h2>
        <h3>
          <a href>To the Video</a>
        </h3>
      </div>
    </div>
  </div>
</template>
<script>
//might not need

export default {
  name: "Home",
  components: {},
  data() {
    return {};
  }
};
</script>
<style lang="scss" scoped>
@import "../assets/style/bowl_shop.scss";
#home {
  a {
    color: #fff;
  }
  #landing-banner {
    background-image: url("../assets/img/home_background.jpg");
    h2 {
      color: #fff;
      padding-top: 10%;
    }
  }
  #promo {
    @include flex(flex, row, wrap, center, center);

    #promo-left {
      background-image: url("../assets/img/dumpling_promo.jpg");
      width: 50%;
      color: #fff;
      h2 {
        margin: auto;
        text-align: left;
        width: 30%;
        padding: 10% 60% 2em 2em;
      }
      h3 {
        margin: auto;
        text-align: left;
        padding-left: 3em;
      }
    }
    #promo-right {
      background-image: url("../assets/img/buddha_promo.jpg");
      width: 50%;
      color: #fff;
      h2 {
        margin: auto;
        text-align: right;
        width: 30%;
        padding: 10% 2em 2em 60%;
      }
      h3 {
        margin: auto;
        text-align: right;
        padding-right: 3em;
      }
    }
  }
}
</style>


