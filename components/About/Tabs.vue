<template>
<div class="wrapper">
  <div class="tabs">
<div class="tab" @click="active_tab=0" :class="{active_tab: active_tab===0 }">Главная</div>
<div class="tab" @click="active_tab=1" :class="{active_tab: active_tab===1 }">Детство</div>
<div class="tab"@click="active_tab=2" :class="{active_tab: active_tab===2 }">Вступление в Stray kids</div>
<div class="tab"@click="active_tab=3" :class="{active_tab: active_tab===3 }">Сейчас</div>
  </div>
  <div class="items">
     <div class="item main" v-if="active_tab===0">
       <p>Феликс (Кор. 필릭스; Яп. フィリックス) - южнокорейско-австралийский рэпер, танцор и ведущий компании JYP Entertainment. Он является участником мужской группы Stray Kids.</p>

     </div>
    <div class="item young" v-if="active_tab===1"> <img src="~/static/images/Lee_Felix_Stray_Kids_profile_photo.png" alt=""></div>
    <div class="item under" v-if="active_tab===2">456</div>
    <div class="item now" v-if="active_tab===3"><h3>I don't care 😎</h3>  <img src="~/static/images/Stray_Kids_Felix_All_In_concept_photo.png" alt=""></div></div>
  </div>
</div>
</template>

<script>
  export default {
    data() {
      return {
        active_tab: 0
      }
    },

  }
</script>

<style lang="scss" scoped>
.wrapper{
  margin-top: 50px;
  opacity: 0.8;

}
.items, .tabs{
   background-color: #fbbbad;
    padding: 0 30px;
}
.tabs{
 position: sticky;
  width: 100%;
  z-index: 400;
  left: 0;
  top: 60px;
  min-height:40px;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  align-items: flex-start;
  border-radius: 4px 4px 0 0;
 border-bottom: 1px solid #4a7a96;
}
.tab{
  cursor: pointer;
  margin-right: 20px;
  padding: 10px 5px;
}
.active_tab{
  background-color: #ee8695;
  border-bottom: 2px solid #4a7a96;
  font-weight: 600;
}
.items{
min-height: 500px;
padding-top: 30px;
}
.young{
  img{
    max-height: 400px;
  }
}
.now{
  text-align: center;
  h3{
    margin-bottom: 20px;
  }
img{
    max-height: 400px;
  }
}

</style>
