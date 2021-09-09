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
    <div class="content-container relative z-10">
      <Nuxt class="content-container__content" />
      <the-side-nav class="content-container__sidenav" />
    </div>
  </div>
</template>
<script>
export default {
  name: 'App',
}
</script>
