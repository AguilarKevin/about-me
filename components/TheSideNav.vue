<template>
  <aside class="flex justify-center">
    <ul>
      <li
        v-for="item in sideNavList"
        :key="item.title"
        class="flex flex-row-reverse items-center gap-3"
        :class="{ 'text-accent': item.checked }"
      >
        <sidebar-item-dot :checked="item.checked" />
        <span>{{ item.title }}</span>
      </li>
    </ul>
  </aside>
</template>

<script>
export default {
  data() {
    return {
      sideNavList: [
        { title: 'Hello!', checked: true },
        { title: 'About me', checked: false },
        { title: 'Skills', checked: false },
        { title: 'Projects', checked: false },
      ],
    }
  },
}
</script>

<style></style>
