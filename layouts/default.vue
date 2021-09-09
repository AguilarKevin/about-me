<template>
  <div class="container">
    <the-header />
    <div class="">
      <Nuxt />
      <the-side-nav />
    </div>
  </div>
</template>
<script>
import TheHeader from '~/components/TheHeader.vue'
export default {
  name: 'App',
  components: { TheHeader },
}
</script>
