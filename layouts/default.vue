<template>
  <div class="default">
    <Navigation />
    <Nuxt />
  </div>
</template>

<script >
import Navigation from "@/components/Navigation/Navigation.vue";

export default {
  components: {
    Navigation,
  },
};
</script>

<style lang="scss">
.default {
  background: url("@/static/images/background-main.jpg") no-repeat center fixed;
  
}
</style>
