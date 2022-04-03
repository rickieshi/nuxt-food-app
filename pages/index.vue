<template>
<main class="container">
  <Header/>
  <ShopInfo/>
</main>
</template>

<script>
import Header from '@/components/Header.vue'
import ShopInfo from '@/components/ShopInfo.vue'
export default {
  name: 'IndexPage',
  components: {
    Header,
    ShopInfo
  }
}
</script>
