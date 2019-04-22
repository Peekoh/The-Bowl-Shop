<template>
  <div id="about">
    <div class="banner">
      <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
          <p>- Name of Person</p>
      </h3>
    </div>
    <div id="about-txt">
      <h2>About Us</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut ut quam nec mauris malesuada luctus. Pellentesque velit dolor, condimentum in bibendum sit amet, aliquet sed dui. Nunc maximus erat eu interdum sollicitudin. Fusce vehicula ante massa, et lobortis odio mollis nec. Praesent ante lectus, faucibus ut mi a, lobortis egestas enim. Sed pulvinar bibendum odio non viverra. Cras tristique accumsan dui, in aliquet ipsum porttitor quis. In hac habitasse platea dictumst. Donec dapibus in nisl non pretium.</p>
      <p>Vestibulum eu pellentesque risus, id varius nibh. Nullam vel ultrices felis. Pellentesque consequat nisi in condimentum interdum. Proin tincidunt gravida sem quis rhoncus. Aenean sem felis, tincidunt eget nisl at, pretium consequat metus. Nam luctus tincidunt auctor. Vivamus laoreet viverra metus. Aliquam erat volutpat. Curabitur convallis dapibus ante, non fringilla nunc tincidunt iaculis. Integer tincidunt dignissim purus, in vehicula neque cursus quis. Etiam sit amet auctor neque, a porttitor nunc.</p>
      <p>Donec quis aliquam quam. Nam rhoncus accumsan enim non semper. Nulla quis lectus leo. Fusce varius nunc dolor, a varius turpis fermentum et. Nunc accumsan imperdiet dolor. Fusce non placerat diam. Sed vitae feugiat sapien. Donec tincidunt laoreet tincidunt. Praesent condimentum fringilla neque, eu bibendum ante mollis sodales. Integer congue nec lorem et dapibus. Ut in leo eu diam suscipit dignissim vel eget massa. Nam rhoncus nibh in malesuada malesuada.</p>
    </div>
  </div>
</template>
<script>
export default {
  name: "About"
};
</script>
<style lang="scss" scoped>
@import "../assets/style/bowl_shop.scss";
#about {
  @include h-w(100%, 100%);
  .banner {
    background-image: url("../assets/img/grandpa_chef.jpg");
@include h-w(100%, 100%);
    h3 {
        width:50%;
      color: #fff;
      margin: auto;
     padding-top:20%;
      font-style:italic;
      p {
          text-align: right;
          padding-right:5em;
      }
    }
  }
  #about-txt {
      padding: 5em;
    @include h-w(auto, 60%);
    margin: auto;
    h2 {
      margin: auto;
      //  padding: 12em 0 3em;
    }
    p{
      line-height: 1.5em;
      padding:.5em;
    }
  }
}
</style>


