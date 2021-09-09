<template>
  <aside
    class="flex justify-center items-center absolute z-20 right-20 inset-y-0"
  >
    <ul class="flex flex-col gap-5">
      <li
        v-for="item in sideNavList"
        :key="item.title"
        class="flex flex-row-reverse items-center gap-3"
        :class="{ 'text-accent': route === item.link }"
      >
        <sidebar-item-dot :checked="route === item.link" />
        <nuxt-link :to="item.link">
          <span>{{ item.title }}</span>
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
        { title: 'Projects', link: '/projects' },
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
