<template>
  <div class="footer">
<div class="wrapper flex">
   <div class="footer-items" >

      <p ><nuxt-link to="/terms-privacy">Политика конфиденциальности</nuxt-link></p>
    </div>
    <div class="footer-items" >
      <p> {{data}} © All rights reserved</p>
    </div>
    <div class="footer-items">
     <a href="http://vk.com/damaroo">Разработчик</a>
    </div>

</div>
  </div>
</template>

<script>
  export default {
data() {
    return {
      data: new Date().getFullYear(),
    }
  },

  }
</script>

<style lang="scss" scoped>
.footer{
  position: sticky;
  width: 100%;
  z-index: 400;
  left: 0;
  bottom: 0,
}
.flex{
  display: flex;
  flex-direction: row;
  justify-content:space-between;
  align-items: center;
  background-color: #292831;
  min-height: 40px;
  padding: 5px 30px;
  border-radius:8px 8px 0 0 ;

}
.footer-items{
  color: #4a7a96;
   font-size: 16px;
}
@media screen and (max-width: 790px) {
.flex{
  flex-direction: column;
  justify-content: space-around;
  min-height: 150px;
  align-items: center;
  text-align: center;
}}
@media screen and (max-width: 400px) {
p{
  font-size: 13px;
  margin-bottom: 10px;
}
}

</style>
