<template>
  <div class="main-container relative">
    <div id="stars-container" class="inset-0 absolute z-0">
      <div id="stars"></div>
      <div id="stars2"></div>
      <div id="stars3"></div>
      <div id="comets">
        <i></i>
        <i></i>
        <i></i>
      </div>
    </div>

    <the-header class="header relative z-10" />
    <Nuxt />
    <the-side-nav />
  </div>
</template>
<script>
export default {
  name: 'App',
}
</script>

<style>
.page-enter-active,
.page-leave-active {
  transition: opacity 0.5s;
}
.page-enter,
.page-leave-to {
  opacity: 0;
}

.layout-enter-active,
.layout-leave-active {
  transition: opacity 0.5s;
}
.layout-enter,
.layout-leave-to {
  opacity: 0;
}
</style>
