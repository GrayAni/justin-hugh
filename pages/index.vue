<template>
  <div class="home">
    <Navbar />
    <Hero />
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import Hero from '@/components/Hero'
export default {
  name: 'HomePage',
  components: {
    Navbar,
    Hero,
  },
}
</script>
<style lang="scss" scoped>
.home {
  min-height: 100vh;
}
</style>
