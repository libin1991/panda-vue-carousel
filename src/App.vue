<template>
  <div class="home">
    <carousel :data="list" :padding="30" :margin="10">
      <img class="step-1" slot-scope="props" :src="props.data.src" alt="" />
    </carousel>
    <div class="hr">-----分割线-----</div>
    <div class="step-2">
      <carousel :data="list">
        <img slot-scope="props" :src="props.data.src" alt="" />
      </carousel>
    </div>
  </div>
</template>

<script>
import Carousel from "./lib/Carousel"

export default {
  name: 'app',
  data () {
    return {
      list: [{
        src: require('./assets/1.jpg')
      }, {
        src: require('./assets/2.jpg')
      }, {
        src: require('./assets/3.jpg')
      }, {
        src: require('./assets/4.jpg')
      }]
    }
  },
  components: {
    Carousel
  }
}
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  img {
    display: block;
    width: 100%;
  }
  .step-1 {
    border-radius: 10px;
  }
  .hr {
    height: 40px;
    line-height: 40px;
    font-size: 14px;
    text-align: center;
  }
  .step-2 {
    position: relative;
  }
  .step-2 .carousel_show_bgcolor {
    background-color: rgb(133, 224, 103);
  }
</style>
