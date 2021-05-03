<template>
  <div class="default">
    <Navigation />
    <Nuxt />
    <Footer/>
  </div>
</template>

<script >
import Navigation from "@/components/Navigation/Navigation.vue";
import Footer from '@/components/Footer/Footer.vue';

export default {
  components: {
    Navigation,
    Footer,
  },
};
</script>

<style lang="scss">
.default {
  background: url("@/static/images/background-main.jpg") no-repeat center fixed;

}
</style>
