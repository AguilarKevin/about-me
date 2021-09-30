<template>
  <aside class="sidenav">
    <ul class="flex flex-1 justify-between md:flex-col gap-8">
      <li
        v-for="item in sideNavList"
        :key="item.title"
        class="flex flex-row-reverse items-center gap-3 transition-all"
        :class="{ 'text-accent animate-pulse ': route === item.link }"
      >
        <sidebar-item-dot
          class="hidden md:block"
          :checked="route === item.link"
        />
        <nuxt-link :to="item.link">
          <span
            class="font-semibold transition-all"
            :class="{
              'md:text-2xl font-bold': route === item.link,
            }"
            >{{ item.title }}</span
          >
        </nuxt-link>
      </li>
    </ul>
  </aside>
</template>

<script>
export default {
  data() {
    return {
      sideNavList: [
        { title: 'Hello!', link: '/' },
        { title: 'About me', link: '/about' },
        { title: 'Skills', link: '/skills' },
      ],
    }
  },
  computed: {
    route() {
      return this.$route.path
    },
  },
}
</script>

<style></style>
