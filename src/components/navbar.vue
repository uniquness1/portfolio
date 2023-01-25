<template>
  <header class="flex items-center justify-between py-5 px-3 md:px-8">
    <div class="logo">
     <a class="" href=""> <h1 class="text-md md:text-xl font-semibold italic font-[cinzel] dark:text-white">Don.<span class="text-[#dc143c]">Uniqueness</span></h1></a>
    </div>
    <div class="flex items-center xs:gap-2 md:gap-3">
      <nav class="nav-menu hidden md:block">
        <a href="#" class="text-xl pl-5 pr-5 pt-1 dark:text-white">About</a>
        <a href="#" class="text-xl pl-5 pr-5 pt-1 dark:text-white">Portfolio</a>
        <a href="#" class="text-xl pl-5 pr-5 pt-1 dark:text-white">Contact</a>
      </nav>
      <div class="space-y-1 mr-2 cursor-pointer md:hidden">
        <span class="block w-7 h-0.5 bg-gray-800 dark:bg-white"></span>
        <span class="block w-6 h-0.5 bg-gray-800 dark:bg-white"></span>
        <span class="block w-5 h-0.5 bg-gray-800 dark:bg-white"></span>
      </div>
      <darkToggle />
    </div>
  </header>
</template>
<script>
import darkToggle from "@/components/darkToggle.vue";
export default {
  name: "navbar",
  data() {
    return {};
  },
  components: {
    darkToggle,
  },
};
</script>
<style scoped>
.nav-menu a {
  position: relative;
  transition: 0.5s;
  font-family: "cinzel", sans-serif;
  font-weight: 500;
}
.nav-menu a::before {
  position: absolute;
  content: "";
  left: 0;
  top: 0;
  width: 100%;
  margin: 0 auto;
  height: 0.2rem;
  background: #dc143c;
  transform: scaleX(0);
  transform-origin: right;
  transition: transform 0.4s linear;
}
.nav-menu a:hover::before {
  transform: scaleX(1);
  transform-origin: left;
  color: #dc143c !important;
}
</style>
