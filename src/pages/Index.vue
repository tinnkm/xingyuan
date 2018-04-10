<template>
  <div>
    <div class="carousel-wrapper" @mouseover="mouseover" @mouseout="mouseout">
      <Carousel :autoplay="autoPlay" v-model="currentItem" loop :autoplay-speed=3000>
        <CarouselItem v-for="(carouse,index) in carouses" :key="index">
          <img :src="carouse.imgUrl" alt="">
          <div class="desc">
            <h3 class="caption">{{ carouse.caption }}</h3>
            <p class="text">{{ carouse.text }}</p>
          </div>
        </CarouselItem>
      </Carousel>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Index',
  data () {
    return {
      autoPlay: true,
      currentItem: 0,
      carouses: [
        {
          imgUrl: 'https://lorempixel.com/1024/480/technics/1/',
          caption: 'First slide',
          text: 'Nulla vitae elit libero, a pharetra augue mollis interdum.'
          // busUrl: 'https://lorempixel.com/1024/480/technics/1/'
        },
        {
          imgUrl: 'https://lorempixel.com/1024/480/technics/2/',
          caption: 'First slide',
          text: 'Nulla vitae elit libero, a pharetra augue mollis interdum.'
          // busUrl: 'https://lorempixel.com/1024/480/technics/1/'
        },
        {
          imgUrl: 'https://lorempixel.com/1024/480/technics/3/',
          caption: 'First slide',
          text: 'Nulla vitae elit libero, a pharetra augue mollis interdum.'
          // busUrl: 'https://lorempixel.com/1024/480/technics/1/'
        },
        {
          imgUrl: 'https://lorempixel.com/1024/480/technics/4/',
          caption: 'First slide',
          text: 'Nulla vitae elit libero, a pharetra augue mollis interdum.'
          // busUrl: 'https://lorempixel.com/1024/480/technics/1/'
        }
      ]
    }
  },
  methods: {
    mouseover () {
      this.autoPlay = false
    },
    mouseout () {
      this.autoPlay = true
    }
  }
}
</script>

<style lang="stylus" scoped>
.carousel-wrapper
  display block
  height 3rem
  width 100%
  & > .ivu-carousel
    height 100%
    width 100%
  &  img
    width 100%;
    height 100%;
    max-width 100%;
    max-height 3rem;
.ivu-carousel-item
  & > .desc
    position relative
    z-index 99999
    top -0.6rem
    & > .caption,.text
      color white

</style>
