<template>
  <div id="app" class="bg-white h-100 dark:bg-black" :class="dark ? 'bg-black dark' : 'light'">
    <navbar />
    <hero />
    <aboutme />
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import navbar from "@/components/navbar.vue"
import hero from "@/components/hero.vue"
import aboutme from "@/components/aboutMe.vue"
export default {
  name: "App",
  components: {
    navbar,
    hero,
    aboutme
  },
  computed: {
    ...mapGetters(["dark"]),
  },
};
</script>

<style></style>
