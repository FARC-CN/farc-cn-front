<template>
  <footer class="bg-white -mt-10 dark:bg-slate-800">
    <div class="container mx-auto">
      <div class="text-center md:text-left">
        <a href="/"
          ><img
            src="/FARC.svg"
            class="animate-bounce h-12 mx-auto mb-8 max-mb:mb-6 hover:animate-none dark:filter dark:invert"
        /></a>
      </div>
      <div class="text-center mb-4">
        <ul class="flex justify-center space-x-3">
          <li v-for="(item, index) in footerItems" :key="item.name">
            <a
              :href="item.link"
              class="text-gray-500 hover:text-gray-900 dark:text-gray-100 hover:dark:text-gray-300"
              >{{ item.name }}</a
            >
            <span
              v-if="index < footerItems.length - 1"
              class="ml-3 dark:text-gray-100"
            >
              ·
            </span>
          </li>
        </ul>
      </div>
    </div>
    <div class="container mx-auto overflow-hidden"></div>
  </footer>
</template>
<script lang="ts">
export default {
  data() {
    return {
      footerItems: [
        {
          name: "首页",
          link: "/",
        },
        {
          name: "Github",
          link: "https://github.com/FARC-CN",
        },
        {
          name: "联系我们",
          link: "mailto:contact@farc.org.cn",
        },
      ],
    };
  },
};
</script>
