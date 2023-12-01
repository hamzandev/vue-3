<template>
  <nav class="bg-blue-500 py-4 shadow">
    <div class="container mx-auto flex items-center justify-between">
      <span class="text-lg font-bold text-white uppercase">Logo</span>
      <div class="flex text-neutral-300 text-lg items-center gap-x-8">
        <a
          v-for="menu in links"
          :key="menu.label"
          class="hover:text-neutral-100 duration-200"
          :href="menu.url"
          >{{ menu.label }}</a
        >
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
export default {
  data: () => {
    return {
      links: [
        { label: "Home", url: "/" },
        { label: "Price", url: "/price" },
        { label: "About", url: "/about" },
        { label: "Contact", url: "/contact" },
      ],
    };
  },
};
</script>
