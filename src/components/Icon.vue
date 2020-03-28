<template>
<div class="icon">
<!--     <li v-for="item in menuItems"
    v-on:click="selected = item"
    v-bind:class="{ selected: selected == item}">
      {{item}}
  </li> -->
  <div class="icon__flex">
    <button class="icon__block" v-on:click="activate(1)">
      <div class="icon__resposive">
        <img src="../assets/content/phone.png"  class="icon__img1">
      </div>
      <div class="icon__center">
        <h4 class="icon__title">Responsive</h4>
        <h5 class="icon__subtitle">Websites</h5>
      </div>
    </button>

    <button class="icon__block" v-on:click="activate(2)">
      <div class="icon__comerce">
        <img src="../assets/content/troley.png"  class="icon__img2">
      </div>
      <div class="icon__center">
        <h4 class="icon__title">e Commerce</h4>
        <h5 class="icon__subtitle">Websites</h5>
      </div>
    </button>

    <button class="icon__block" v-on:click="activate(3)">
      <div class="icon__daily">
        <img src="../assets/content/earth.png"  class="icon__img3">
      </div>
      <div class="icon__center">
        <h4 class="icon__title">Daily blog</h4>
        <h5 class="icon__subtitle">Websites</h5>
      </div>
    </button>

    <button class="icon__block" v-on:click="activate(4)">
      <div class="icon__search">
        <img src="../assets/content/search.png"  class="icon__img4">
      </div>
      <div class="icon__center">
        <h4 class="icon__title">Search based</h4>
        <h5 class="icon__subtitle">Websites</h5>
      </div>
    </button>
  </div>
  <div class="icon__subblock">
    <div class="icon__subshow" v-if="active(1)">
      <img src="../assets/content/exp.png" class="icon__imgbig1">
      <h4 class="icon__title2">Lorem Ipsum is simply dummy text111</h4>
      <p class="icon__text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the "1500s", when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has  survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.It was popularised in the "1960s" with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the "1500s", when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the "1960s" with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
    </div>
    <div class="icon__subshow" v-if="active(2)">
      <img src="../assets/content/exp.png" class="icon__imgbig2">
      <h4 class="icon__title2">Lorem Ipsum is simply dummy text222</h4>
      <p class="icon__text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the "1500s", when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has  survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.It was popularised in the "1960s" with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the "1500s", when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the "1960s" with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
    </div>
    <div class="icon__subshow" v-if="active(3)">
      <img src="../assets/content/exp.png" class="icon__imgbig3">
      <h4 class="icon__title2">Lorem Ipsum is simply dummy text333</h4>
      <p class="icon__text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the "1500s", when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has  survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.It was popularised in the "1960s" with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the "1500s", when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the "1960s" with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
    </div>
    <div class="icon__subshow" v-if="active(4)">
      <img src="../assets/content/exp.png" class="icon__imgbig4">
      <h4 class="icon__title2">Lorem Ipsum is simply dummy text444</h4>
      <p class="icon__text">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the "1500s", when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has  survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.It was popularised in the "1960s" with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the "1500s", when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the "1960s" with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
    </div>
  </div>
</div>
</template>
<script>
export default {
  name: 'Icon',
  data () {
    return {
      show: new Set([1])
    }
  },
  methods: {
    activate (index) {
      // if (this.show.has(index)) {
      //   this.show.delete(index)
      // } else {
      //   this.show.add(index)
      // }
      this.show = new Set([index])
    },
    active (index) {
      return this.show.has(index)
    }
  }
}
</script>
<style lang="scss">
.icon {
  &__block {
    border: 1px solid transparent;
    border-bottom: none;
    padding: rem(52);
    // transition-duration: .5s;
  }
  &__flex {
    @include FCenter(space-around);
  }
  &__block:focus {
    border-color: $border;
    // background-color: red;
    outline: none;
  }
  &__resposive:hover, &__comerce:hover, &__daily:hover, &__search:hover, &__title:hover, &__subtitle:hover {
    cursor: pointer;
  }
  &__resposive, &__comerce, &__daily, &__search {
    position: relative;
  }
  &__img1, &__img2, &__img3, &__img4,{
    position: absolute;
    z-index: 1;
    left: 30%;
    outline: none;
  }
  &__img3 {
    left: 18%;
    top: -5%;
  }
  &__img4 {
    left: 27%;
    top: 5%;
  }
  &__center {
    text-align: center;
    margin-top: rem(55);
  }
  &__title {
    display: inline-block;
    font-size: rem(22);
    font-weight: normal;
  }
  &__subtitle {
    display: inline-block;
    font-size: rem(20);
    font-weight: lighter;
  }

  &__subshow {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: rem(40) rem(30) rem(60);
    border: 1px solid $before;
    border-top: none;
  }
  &__imgbig1, &__imgbig2, &__imgbig3, &__imgbig4 {
    margin: 0 0 rem(40);
    position: relative;
  }
  &__imgbig1:before, &__imgbig2:before, &__imgbig3:before, &__imgbig4:before {
    position: absolute;
    content: "";
    height: 1px;
    // background-color: $before;
  }
  &__imgbig1:before {
    width: rem(100);
    top: 0;
  }
  &__title2 {
    font-size: rem(35);
    font-weight: normal;
    opacity: 0.7;
    margin: 0 0 rem(20) 0;

  }
  &__text {
    font-size: rem(14);
    opacity: 0.6;
    font-weight: lighter;
  }

}
@include Hexagon(icon__resposive, 140px, 80px, $blue, 70px, 40px);
@include Hexagon(icon__comerce, 140px, 80px, $yellow, 70px, 40px);
@include Hexagon(icon__daily, 140px, 80px, $lightgreen, 70px, 40px);
@include Hexagon(icon__search, 140px, 80px, $orange, 70px, 40px);
</style>
