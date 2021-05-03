<template>
<div class="wrapper">
  <div class="tabs">
<div class="tab" @click="active_tab=0" :class="{active_tab: active_tab===0 }">Главная</div>
<div class="tab" @click="active_tab=1" :class="{active_tab: active_tab===1 }">Детство</div>
<div class="tab"@click="active_tab=2" :class="{active_tab: active_tab===2 }">Вступление в Stray kids</div>
<div class="tab"@click="active_tab=3" :class="{active_tab: active_tab===3 }">Сейчас</div>
  </div>
  <div class="items">
    <!-- <transition name="fade" mode="in"> -->
     <div class="item main" v-if="active_tab===0">
       <div class="flex">
       <p>    Stage name: <b> Felix</b> </p>
       <p>Birth Name:<b> Felix Lee, Lee Yongbok</b> </p>
       <p>Korean Name:<b> Lee Yong Bok</b> </p>
       <p>Position:<b> Lead Dancer, Lead Rapper, Sub-Vocalist</b> </p>
       <p>Birth Date:<b> September 15, 2000 (age {{age}}</b> </p>
       <p>Birth Place: <b>Sydney, Australia</b> </p>
       <img src="~/static/images/main-felix.jpg" alt="">

       </div>

       <iframe src="https://www.youtube.com/embed/A76WWeiskSk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

     </div>
    <div class="item young" v-if="active_tab===1"> <img src="~/static/images/Lee_Felix_Stray_Kids_profile_photo.png" alt=""></div>
    <div class="item under" v-if="active_tab===2"><p>
    <b>  2018: Дебют в Stray Kids</b><br>
25 марта 2018 года Феликс дебютировал в Stray Kids, компании JYP Entertainment с мини-альбомом I Am Not.<br>
 Выбыл в 8 эпизоде, но потом вернулся в 9 эпизоде.</p></div>
    <div class="item now" v-if="active_tab===3">
      <h3>I don't care 😎</h3>
       <img src="~/static/images/Stray_Kids_Felix_All_In_concept_photo.png" alt="">
       </div>
        </div>
  </div>



</div>
</template>

<script>
export default {
  data() {
    return {
      active_tab: 0,
      age: 20,
    };
  },

  computed: {},
};
</script>

<style lang="scss" scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}

.wrapper {
  margin-top: 50px;
  opacity: 0.9;
}
.items,
.tabs {
  background-color: #fbbbad;
  padding: 0 30px;
}
.tabs {
  position: sticky;
  width: 100%;
  z-index: 400;
  left: 0;
  top: 60px;
  min-height: 40px;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  align-items: flex-start;
  border-radius: 4px 4px 0 0;
  border-bottom: 1px solid #4a7a96;
}
.tab {
  cursor: pointer;

  padding: 10px 20px;
}
.active_tab {
  background-color: #ee8695;
  border-bottom: 2px solid #4a7a96;
  font-weight: 600;
}
.items {
  min-height: 500px;
  padding-top: 30px;
}
.main {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;
  width: 100%;
  iframe{
aspect-ratio: 16/9;
width: 70%;
  }
  img{
    width: 350px;
    margin-top: 20px;
    margin-bottom: 50px;
  }
  p{
    margin-bottom: 10px;
  }
}
.young {
  text-align: center;
  img {
    max-height: 400px;
  }
}
.now {
  text-align: center;
  h3 {
    margin-bottom: 20px;
  }
  img {
    max-height: 400px;
  }
}
</style>
