<template>
<div class="Whyus">
  <div class="Whyus__img"></div>
  <div class="Whyus__block">
    <div class="Whyus__title">Why choose us ?</div>
    <div class="Whyus__flex" v-for="w in whys" :key="w.id">
      <img :src=" require('../assets/content/' + w.img) ">
      <p class="Whyus__text">{{ w.text }}</p>
    </div>

  </div>
</div>
</template>

<script>
export default {
  name: 'Whyus',
  data () {
    return {
      whys: [
        { id: 1, text: 'Lorem Ipsum is simply dummy text of the printing and typesetting', img: 'tick.png' },
        { id: 2, text: 'Lorem Ipsum has been the industrys standard dummy text ever', img: 'tick.png' },
        { id: 3, text: 'When an unknown printer took a galley of type and scrambled', img: 'tick.png' },
        { id: 4, text: 'It has survived not only five centuries, but also the leap into electronic', img: 'tick.png' },
        { id: 5, text: 'It was popularised in the 1960s with the release of Letraset sheets containing', img: 'tick.png' },
        { id: 6, text: 'More recently with desktop publishing software like Aldus PageMaker', img: 'tick.png' }
      ]
    }
  }
}
</script>

<style lang="scss">
.Whyus {
  padding: rem(20) 0 rem(70);
  @include FCenter(space-between);
  &__flex {
    @include FCenter(flex-start);
    padding: rem(5) 0;
    width: rem(500);
  }
  &__title {
    padding-bottom: rem(25);
    font-size: rem(30);
    font-weight: normal;
  }
  &__img {
    background: url('../assets/content/brouser.png') center;
    width: rem(450);
    height: rem(320);
  }
  &__text {
    padding-left: rem(10);
  }
}
</style>
