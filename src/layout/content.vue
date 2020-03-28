<template>
<div class="Content">
  <div class="wrapper">
    <Icon/>
    <Whyus/>
  </div>
  <Logsub/>
</div>
</template>

<script>
import Icon from '@/components/Icon.vue'
import Logsub from '@/components/Logsub.vue'
import Whyus from '@/components/Whyus.vue'
export default {
  name: 'Content',
  components: {
    Icon,
    Whyus,
    Logsub
  }
}
</script>

<style lang="scss">
.Content {
  padding: rem(50) 0 rem(30);
}
</style>
