<template>
  <div class="wrapper">
    <div class="photos">
      <div class="title">
        <h2>Most popular photos</h2>
      </div>
      <div class="images" v-if="photos">
        <splide :options="primaryOptions" ref="primary">
          <splide-slide v-for="item in photos" :key="item.id">
            <img :src="require(`~/static/images/${item.link}`)" alt="Зайка" />
          </splide-slide>
        </splide>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      primaryOptions: {
        type: "loop",
        rewind: true,
        width: "100%",
        pagination: false,
        perPage: 4,
        perMove: 1,
        arrows: true,
        autoWidth: true,
        gap: 20,
        autoplay: true,
        interval: 2000,
      },
      photos:[{
        id: 1, link: 'felix-1.jpg'
      },{
        id: 2, link: 'felix-2.jpg'
      },{
        id: 3, link: 'felix-3.jpg'
      },{
        id: 4, link: 'felix-4.jpg'
      },{
        id: 5, link: 'felix-5.jpg'
      },{
        id: 6, link: 'felix-6.jpg'
      },{
        id: 7, link: 'felix-7.jpg'
      },{
        id: 8, link: 'felix-8.jpg'
      },{
        id: 9, link: 'felix-9.png'
      },{
        id: 10, link: 'felix-10.jpeg'
      },{
        id: 11, link: 'felix-11.jpg'
      }]
    };
  },
};
</script>

<style lang="scss" scoped>
.photos {
padding-bottom: 500px;
}
.title {
  color: #ee8695;
  margin-top: 50px;
  font-size: 38px;
}
.images {
  margin-top: 50px;
}
.splide__slide{
 max-width: 300px;
  max-height: 400px;
  border: 2px solid #292831;

  overflow: hidden;
   -webkit-box-shadow: 0px 20px 18px -13px rgba(41, 40, 49, 0.7);
-moz-box-shadow: 0px 20px 18px -13px rgba(41, 40, 49, 0.7);
box-shadow: 0px 20px 18px -13px rgba(41, 40, 49, 0.7);
}
img {
 width:100%;
 height: 100%;
 object-fit:cover;

}
</style>
