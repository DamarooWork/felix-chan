<template>
  <div class="navigation-block">
    <div class="wrapper flex">
      <div class="left-links">
        <nuxt-link class="tab" to="/">Home</nuxt-link>
        <nuxt-link class="tab" to="/about">About</nuxt-link>
        <nuxt-link class="tab" to="/photos">Photos</nuxt-link>
        <nuxt-link class="tab" to="/interview">Interview</nuxt-link>
      </div>
      <div class="right-links">
        <nuxt-link class="tab" to="/">by Damaroo</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
  }),
};
</script>

<style lang="scss" scoped>
.flex {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  background-color: #292831;
  min-height: 50px;
  padding: 18px 30px;
  border-radius: 0 0 8px 8px;
  -webkit-box-shadow: 0px 6px 24px 3px rgba(41, 40, 49, 0.4);
  -moz-box-shadow: 0px 6px 24px 3px rgba(41, 40, 49, 0.4);
  box-shadow: 0px 6px 24px 3px rgba(41, 40, 49, 0.4);
}
.navigation-block {
  position: sticky;
  width: 100%;
  z-index: 400;
  left: 0;
  top: 0;
}
.left-links {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  .tab {
    font-weight: 700;
    margin-right: 20px;
  }
}
.right-links {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  .tab {
    margin-left: 20px;
  }
}
.tab {
  font-size: 22px;
  color: #fbbbad;
}
</style>
