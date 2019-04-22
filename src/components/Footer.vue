<template>
  <footer>
    <ul class="footer-links">
      <li>Link 1</li>
      <li>Link 2</li>
      <li>Link 3</li>
    </ul>
    <p>Made by
      <a href="http://dana-hedrick.com">Dana Hedrick</a>
    </p>
  </footer>
</template>
<script>
export default {
  name: "Footer"
};
</script>
<style lang="scss" scoped>
@import "../assets/style/bowl_shop.scss";
footer {
  margin:0;
  padding: 2em;
  position: relative;
  bottom: 0;
  width: 100%;
  height:6em;
  color: #fff;
  @include h-w(75px, 100%);
  background: #000;
  .footer-links {
    width:100%;
    @extend %reset;
    list-style: none;
    @include flex(flex, row, wrap, center, flex-end);
    li {
      padding: 0 0.3em;
    }
  }
  p {
    padding-right:3em;
    font-size: 0.8em;
    text-align: right;
    a {
      color: #fff;
      text-decoration: none;
    }
  }
}
</style>
