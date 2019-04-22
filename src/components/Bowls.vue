<template>
  <div id="menu">
    <div id="bowls">
      <a href class="menu-item" 
        @mouseover="activethumb = 1" 
        v-bind:class="[ activethumb === 1 ? 'activethumb' : '' ]"
        @mouseleave="activethumb = 0" 
        @click.prevent>
        <span class="img-description" v-if="activethumb === 1">Complete Ramen<sub>$9</sub></span>
        <img src="../assets/bowls/complete_ramen.jpg" alt="Complete Ramen">
      </a>
      <a href class="menu-item" 
        @mouseover="activethumb = 2" 
        v-bind:class="[ activethumb === 2 ? 'activethumb' : '' ]"
        @mouseleave="activethumb = 0" 
        @click.prevent>
        <span class="img-description" v-if="activethumb === 2">Dumpling Soup<sub>$12</sub></span>
        <img src="../assets/bowls/dumpling_soup.jpg" alt="Dumpling Soup">
      </a>
      <a href class="menu-item" 
        @mouseover="activethumb = 3" 
        v-bind:class="[ activethumb === 3 ? 'activethumb' : '' ]"
        @mouseleave="activethumb = 0" 
        @click.prevent>
        <span class="img-description" v-if="activethumb === 3">Miso Noodle Soup<sub>$6</sub></span>
        <img src="../assets/bowls/miso_noodle.jpg" alt="Miso Noodle Soup">
      </a>
      <a href class="menu-item" 
        @mouseover="activethumb =4" 
        v-bind:class="[activethumb === 4? 'activethumb':'']"
        @mouseleave="activethumb = 0" 
        @click.prevent>
        <span class="img-description" v-if="activethumb ===4">Shroomy Ramen<sub>$9</sub>
        </span>
        <img src="../assets/bowls/mushroom_ramen.jpg" alt="Shroomy Ramen">
      </a>
      <a href class="menu-item" 
        @mouseover="activethumb = 5" 
        v-bind:class="[activethumb === 5 ? 'activethumb':'']"
        @mouseleave="activethumb = 0" 
        @click.prevent>
        <span class="img-description" v-if="activethumb === 5">Seafood Curry<sub>$10</sub></span>
        <img src="../assets/bowls/shrimp_curry.jpg" alt="Seafood Curry">
      </a>
      <a href class="menu-item" 
        @mouseover="activethumb = 6" 
        v-bind:class="[activethumb === 6 ? 'activethumb':'']"
        @mouseleave="activethumb = 0" 
        @click.prevent>
        <span class="img-description" v-if="activethumb === 6">Udon Noodle Bowl<sub>$8</sub></span>
        <img src="../assets/bowls/udon_soup.jpg" alt="Udon Noodle Bowl">
      </a>
    </div>
    <div id="drinks-and-extras">
      <ul>
        <h2>Drink Menu</h2>
        <li>
          Green Tea
          <span>$2</span>
        </li>
        <li>
          Melon Soda
          <span>$2</span>
        </li>
        <li>
          Orange Juice
          <span>$3</span>
        </li>
        <li>
          Sparkling Water
          <span>$3</span>
        </li>
        <li>
          Thai Tea
          <span>$4</span>
        </li>
      </ul>
      <ul>
        <h2>Sides/Extras</h2>
        <li>
          Buddha Style*
          <span>$0</span>
        </li>
        <li>
          Seasonal Fruit
          <span>$3</span>
        </li>
        <li>
          Daifuku Mochi
          <span>$5</span>
        </li>
        <li>
          Spicy Edamame
          <span>$2</span>
        </li>
      </ul>
      <sub>*Order one of our bowls Buddha Style for a plant-based meal, made with homemade seitan or tofu.</sub>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Bowls",
    data() {
      return {
        activethumb: 0
      };
    }
  };
</script>
<style lang="scss" scoped>
  @import "../assets/style/bowl_shop.scss";

  #menu {
    @include flex(flex, row, wrap, center, center);
    @include h-w(100%, 100%);
    @extend %reset;

    #bowls {
      @extend %reset;
      @include h-w(100%, 65%);
      @include flex(flex, row, wrap, center, flex-start);

      .menu-item {
        position: relative;
        margin: 1em;
        cursor: default;
        @include h-w(20em, 20em);
        @extend %reset;

        .img-description {
          @extend %reset;
          @include flex(flex, column, none, center, center);
          @include h-w(inherit, inherit);
          position: absolute;
          opacity: 0;
          color: #000;
          font-family: $font-head;
          font-weight: bolder;
          font-size: 1.5em;
          text-align: center;
          transition: opacity 0.7s;

          // border:black solid 1px;
          sub {
            align-self: center;


          }
        }

        img {
          object-fit: cover;
          @include h-w(inherit, inherit);
          transition: opacity 0.7s;
        }
      }

      .activethumb .img-description {
        @extend %reset;
        z-index: 1;
        opacity: 1;
      }

      .activethumb img {
        opacity: 0.5;
        @extend %reset;
      }
    }

    #drinks-and-extras {
      @include h-w(50%, 15%);
      align-self: flex-start;

      @extend %reset;
      text-align: center;

      ul {
        padding: 3em;

        li {
          list-style: none;

          span {
            float: right;
          }
        }
      }

      sub {
        font-size: 0.7em;
      }
    }
  }
</style>