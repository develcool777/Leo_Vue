<template>
  <div class="header">
    <div class="header__logo">Leo/-</div>
    <nav class="header__menu">
      <a :href="item.href" class="header__link" v-for="item in items" :key="item.id">{{ item.title }}</a>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Menu',
  data () {
    return {
      items: [
        { id: 1, title: 'Solutions', href: '#Solutions' },
        { id: 2, title: 'Products', href: '#Products' },
        { id: 3, title: 'Portfolio', href: '#Portfolio' },
        { id: 4, title: 'Contact', href: '#Contact' }
      ]
    }
  }
}
</script>

<style lang="scss">
.header {
  @include FCenter(space-between);
  &__logo{
    display: inline-block;
    color: $white;
    font-size: rem(80);
    font-weight: bold;
  }
  @include LinkShort(none, $white);
  &__menu {
    width: rem(450);
    @include FCenter(space-between);
    transition-duration: .5s;
  }
  &__menu:hover {
    color: red;
  }
  &__link {
    font-weight: normal;
    font-size: rem(20);
  }
}
</style>
