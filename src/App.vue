<template>
  <div id="app" class="bg-white h-100 dark:bg-black" :class="dark ? 'bg-black dark' : 'light'">
    <navbar />
    <hero />
  </div>
</template>

<script>
import { mapGetters } from "vuex";
import navbar from "@/components/navbar.vue"
import hero from "@/components/hero.vue"
export default {
  name: "App",
  components: {
    navbar,
    hero
  },
  computed: {
    ...mapGetters(["dark"]),
  },
};
</script>

<style></style>
