<template>
  <div class="Slider">
    <div class="Slider__wrap">
      <div class="Slider__flex" :style="{'margin-left': '-' + (750 * currentslide) + 'px'}">
        <Myslide
        v-for="item in data"
        :key="item.id"
        :slideritem="item"
        />
      </div>
    </div>
    <a class="Slider__left">
      <div class="Slider__prev" @click="prevSlide"></div>
    </a>
    <a class="Slider__right">
      <div class="Slider__next" @click="nextSlide"></div>
    </a>
  </div>
</template>
<script>
import Myslide from '@/components/SliderItem'
export default {
  name: 'Slider',
  components: {
    Myslide
  },
  props: {
    data: Array,
    default: () => []
  },
  data () {
    return {
      currentslide: 0
    }
  },
  methods: {
    prevSlide () {
      if (this.currentslide > 0) {
        this.currentslide--
        console.log(this.currentslide)
      }
    },
    nextSlide () {
      if (this.currentslide >= this.data.length - 1) {
        this.currentslide = 0
        console.log(this.currentslide)
      } else {
        this.currentslide++
      }
    }
  }
}
</script>
<style lang="scss">
.Slider {
  width: 100%;
  height: rem(300);
  padding: rem(30) 0 0;
  position: relative;
  @include Arrows();
  &__wrap {
    margin: 0 auto;
    width: rem(750);
    overflow: hidden;
  }
  &__flex {
    display: inline-flex;
    transition: all ease .5s;
  }
  &__left {
    position: absolute;
    top: 50%;
    left: rem(80);
  }
  &__right {
    position: absolute;
    top: 50%;
    right: rem(80);
  }
}
</style>
