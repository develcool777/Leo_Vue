<template>
<div class="">
  <Header/>
  <Content/>
  <Footer/>
</div>
</template>

<script>
import Header from '@/layout/header'
import Content from '@/layout/content'
import Footer from '@/layout/footer'
export default {
  name: 'HomePage',
  // data () {
  //   return {
  //     posts: [
  //       { id: 1, title: ',smcpu', subtitle: 'Subbbb' },
  //       { id: 2, title: ',sdlef', subtitle: 'Subbbb' },
  //       { id: 3, title: ',13243', subtitle: 'Subbbb' },
  //       { id: 4, title: ',,rmvo', subtitle: 'Subbbb' }
  //     ]
  //   }
  // },
  components: {
    Header,
    Content,
    Footer
  }

}
</script>

<style lang="scss">

</style>
