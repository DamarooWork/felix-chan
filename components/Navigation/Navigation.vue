<template>
  <div class="navigation-block">
    <div class="wrapper flex">
      <div class="left-links" >
        <nuxt-link v-for="item in links" :key="item.id" exact-active-class="tab_active" class="tab" :to="item.link"
          ><p>{{item.name}}</p></nuxt-link>
      </div>
      <div class="right-links">
        <a class="tab" href="http://vk.com/damaroo" target="_blank">by Damaroo-chan</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    links: [
      {
        id: 1,
        name: "Felix",
        link: "/",
      },
      {
        id: 2,
        name: "About",
        link: "/about",
      },
      {
        id: 3,
        name: "Photos",
        link: "/photos",
      },
      {
        id: 4,
        name: "Interview",
        link: "/interview",
      },
    ],
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
  padding: 10px 30px;
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
  position: relative;
  text-align: center;
  align-self: center;
  box-sizing: border-box;
  padding: 5px 10px;
  min-height: 30px;
  font-size: 22px;
  color: #fbbbad;
  transform: scale(1);
  transition: all 0.5s;
  border-radius: 8px;
  p {
    transition: all 0.5s;
  }
  &:hover {
    background-color: rgba(74, 122, 150, 0.7);
  }
  &:active {
    color: #ee8695;
  }
}
.tab_active {
  color: #ee8695;
  p {
    transition: all 0.5s;
  }
}
</style>
