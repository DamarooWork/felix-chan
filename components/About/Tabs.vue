<template>
<div class="wrapper">
  <div class="tabs">
<div class="tab" @click="active_tab=0" :class="{active_tab: active_tab===0 }">Главная</div>
<div class="tab" @click="active_tab=1" :class="{active_tab: active_tab===1 }">Детство</div>
<div class="tab" @click="active_tab=2" :class="{active_tab: active_tab===2 }">Вступление в Stray kids</div>
<div class="tab" @click="active_tab=3" :class="{active_tab: active_tab===3 }">Сейчас</div>
  </div>
  <div class="items">

     <div class="item main" v-if="active_tab===0">
       <div class="content">
       <p>    Stage name: <b> Felix</b> </p>
       <p>Birth Name:<b> Felix Lee, Lee Yongbok</b> </p>
       <p>Korean Name:<b> Lee Yong Bok</b> </p>
       <p>Position:<b> Lead Dancer, Lead Rapper, Sub-Vocalist</b> </p>
       <p>Birth Date:<b> September 15, 2000 (age {{age}})</b> </p>
       <p>Birth Place: <b>Sydney, Australia</b> </p>
       <img src="~/static/images/main-felix.jpg" alt="Felix">
       </div>
        <div class="video">
         <iframe src="https://www.youtube.com/embed/A76WWeiskSk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
     </div>
     <div class="item young" v-if="active_tab===1">
      <p> <b> Ли Феликс</b> родился в корейской семье в Сиднее 15 сентября 2000 года.</p>
        <p> Детство будущей звезды прошло в Австралии. На родном языке его имя звучит как Ли Ен Бок, но парень признается, что привык к австралийскому варианту – Ли Феликс.</p>
        <p>  Мальчик рос вместе с двумя родными сестрами. Образование получил в католическом колледже Святого Патрика.</p>
         <p>  В свободное от учебы время молодой человек увлекался плаванием, тхэквондо и игрой на пианино.</p>
         <p>   Однажды Ли даже принял участие в соревнованиях по плаванию, где занял призовое место.</p>
          <div class="photos">
            <div class="photo"><img src="~/static/images/felix-young-1.jpg" alt="Felix"></div>
            <div class="photo"><img src="~/static/images/Lee_Felix_Stray_Kids_profile_photo.png" alt=""></div>
            <div class="photo"><img src="~/static/images/felix-young-2.jpg" alt="Felix"></div>
        </div>
      </div>
    <div class="item under" v-if="active_tab===2">
     <p> <b>  2018: Дебют в Stray Kids</b><br>
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
  color: #292831;
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
  -webkit-box-shadow: 0px 6px 12px 3px rgba(41, 40, 49, 0.3);
  -moz-box-shadow: 0px 6px 12px 3px rgba(41, 40, 49, 0.3);
  box-shadow: 0px 6px 12px 3px rgba(41, 40, 49, 0.3);
}
.tab {
  cursor: pointer;
  padding: 10px 20px;
  &:hover {
    background-color: #f39fad;
    border-bottom: 2px solid #4a7a96;
  }
}
.active_tab {
  background-color: #ee8695;
  border-bottom: 2px solid #4a7a96;
  font-weight: 600;
  &:hover {
    background-color: #ee8695;
    border-bottom: 2px solid #4a7a96;
  }
}
.items {
  min-height: 500px;
  padding-top: 30px;
  border-radius: 0 0 4px 4px;
}
.main {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;

  .content {
    font-size: 20px;
    width: 30%;
    margin-right: 5%;
  }
  .video {
    aspect-ratio: 16/9;
    width: 65%;
    iframe {
      width: 100%;
      aspect-ratio: 16/9;
    }
  }
  img {
    width: 350px;
    margin-top: 20px;
    margin-bottom: 50px;
  }
  p {
    margin-bottom: 10px;
  }
}
.young {
  font-size: 20px;
  p {
    margin-bottom: 10px;
  }
  img {
    margin-top: 20px;
    max-height: 400px;
    margin-bottom: 50px;
  }
  .photos {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
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
