<template>
  <div class="justin-hughes">
    <div class="justin-hughes__content">
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
  name: 'DefaultComp',
}
</script>
<style lang="scss" scoped>
.justin-hughes {
  width: 100%;
  min-height: 100vh;
  background: #f0e1bc;

  &__content {
    position: relative;
    max-width: 1900px;
    margin: 0 auto;
  }
}
</style>
