<template>
  <div class="head">
    <div class="wrapper">
      <Menu/>
    </div>
    <Slider :data="Sitems"/>
  </div>
</template>

<script>
import Menu from '@/components/Menu'
import Slider from '@/components/Slider'
export default {
  name: 'Header',
  components: {
    Menu,
    Slider
  },
  data () {
    return {
      Sitems: [
        { id: 1, title: 'Introducing', subtitle: 'Something hot......', btn: 'Try Demo', url: 'icon.png' },
        { id: 2, title: 'Products', subtitle: 'Something cold......', btn: 'Try Dem', url: 'icon.png' },
        { id: 3, title: 'Portfolio', subtitle: 'Something wet......', btn: 'Try De', url: 'icon.png' },
        { id: 4, title: 'Contact', subtitle: 'Something dirty......', btn: 'Try D', url: 'icon.png' }
      ]
    }
  }
}
</script>
<style lang="scss">
.head {
  background: url('../assets/header/bg.png');
  background-size: cover;
}
</style>
