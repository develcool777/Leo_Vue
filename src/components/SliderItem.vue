<template>
  <div class="Myslide">
    <div class="Myslide__block1">
      <img :src=" require('../assets/header/' + slideritem.url ) "  class="Myslide__img">
    </div>
    <div class="Myslide__block2">
      <div class="Myslide__title">{{ slideritem.title }}</div>
      <div class="Myslide__subtitle">{{slideritem.subtitle}}</div>
      <button class="Myslide__btn">{{slideritem.btn}}</button>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Myslide',
  props: {
    slideritem: {
      type: Object,
      default: () => {}
    }
  }
}
</script>
<style lang="scss">
.Myslide {
  display: flex;
  justify-content: space-between;
  position: relative;
  width: rem(750);

  &__title {
    font-size: rem(60);
    color: $white;
  }
  &__subtitle {
    margin: rem(10) 0 rem(25);
    font-size: rem(35);
    color: $white;
  }
  &__block1 {
    position: relative;
    width: rem(354);
    height: rem(345);
  }
  &__block2 {
    padding: rem(60) rem(45) 0;
  }
  &__img {
    position: absolute;
    left: 0;
    top: 0;
    border: none;
  }
  &__btn {
    padding: rem(5) rem(20);
    background-color: $green;
    border: 2px solid rgba(0, 0, 0, 0.5);
    border-radius: rem(2);
    outline: none;
    color: $white;
    font-size: rem(20);
    transition-duration: .5s;
  }
  &__btn:hover {
    border: 2px solid rgba(0, 0, 0, 1);
    cursor: pointer;
    color: $green;
    background-color: $white;
  }
}
</style>
