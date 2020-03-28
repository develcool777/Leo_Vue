<template>
<div class="Footer">
  <div class="wrapper">
    <div class="Footer__flex">
      <div class="Footer__menu" v-for="m in menuItems" :key="m.id">
        <div class="Footer__title">{{ m.title }}</div>
        <div class="Footer__item">{{ m.text1 }}</div>
        <div class="Footer__item">{{ m.text2 }}</div>
        <div class="Footer__item">{{ m.text3 }}</div>
        <div class="Footer__item">{{ m.text4 }}</div>
        <div class="Footer__item">{{ m.text5 }}</div>
        <div class="Footer__item">{{ m.text6 }}</div>
      </div>
      <div class="Footer__left">
        <div class="Footer__prev"></div>
      </div>
      <div class="Footer__right">
        <div class="Footer__next"></div>
      </div>
      <div class="Footer__block">
        <div class="Footer__logo">Leo/-</div>
        <div class="Footer__link">© cssauthor.com</div>
      </div>
    </div>
    <div class="arrow"></div>
  </div>
</div>
</template>

<script>
export default {
  name: 'Footer',
  data () {
    return {
      menuItems: [
        { id: 1, title: 'About Us', text1: 'About us', text2: 'Customer Stories', text3: 'Customer Stories', text4: 'Press Resources', text5: 'Press Releases', text6: 'Contact us' },
        { id: 2, title: 'About Us', text1: 'About us', text2: 'Customer Stories', text3: 'Customer Stories', text4: 'Press Resources', text5: 'Press Releases', text6: 'Contact us' },
        { id: 3, title: 'Testimoanials', text1: 'Lorem Ipsum is simply dummy text of the printing and ', text2: 'typesetting industry. Lorem Ipsum has been the industr', text3: 'standard dummy text ever since the 1500s,', text4: 'when an unknown printer took a ', text5: 'Lorem Ipsum is simply', text6: 'Owner, Lorem Ipsum' }
      ]
    }
  }
}
</script>

<style lang="scss">
.Footer {
  background: url('../assets/footer/backfoot.png');
  color: white;
  padding: rem(35) 0;
  &__flex {
    @include FCenter(space-between);
    padding: 0 rem(20);
  }
  &__title {
    font-size: rem(22);
    margin-bottom: rem(15);
  }
  &__item {
    font-size: rem(13);
    margin: rem(5) 0;
    transition-duration: .5s;
  }
  &__item:hover {
    cursor: pointer;
    color: $lightgreen;
  }
  &__logo {
    font-size: rem(100);
  }
  &__prev, &__next {

  }
}
.arrow {
  // display: block;
  position: absolute;
  top: 20px;
  // right: 400px;
  // width: 56px;
  // height: 1px;
  // background-color: green;
}

.arrow:before {
  content: '';
  display: block;
  position: absolute;
  top: 0;
  right: 0;
  width: 10px;
  height: 1px;
  background-color: red;
  transform: rotate(-45deg);
  transform-origin: 100% 0%;
}

.arrow:after {
  content: '';
  display: block;
  position: absolute;
  top: 0;
  right: 0;
  width: 10px;
  height: 1px;
  background-color: red;
  transform: rotate(45deg);
  transform-origin: 100% 0%;
}
</style>
