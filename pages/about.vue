<template>
  <div class="about">
    <Tabs />
  </div>
</template>

<script>
import Tabs from "../components/About/Tabs.vue";

export default {
  components: {
    Tabs,
  },
};
</script>

<style lang="scss" scoped>
.about {
  min-height: 1000px;
}
</style>
