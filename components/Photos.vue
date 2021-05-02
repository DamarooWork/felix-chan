<template>
  <div class="wrapper">
    <div class="photos">
      <div class="title">
        <h2>Most popular photos</h2>
      </div>
      <div class="images">
        <splide :options="primaryOptions" ref="primary">
          <splide-slide>
            <img src="~/static/images/felix-1.jpg" alt="Зайка" />
          </splide-slide>
          <splide-slide>
            <img src="~/static/images/felix-2.jpg" alt="Зайка" />
          </splide-slide>
          <splide-slide>
            <img src="~/static/images/felix-3.jpg" alt="Зайка" />
          </splide-slide>
           <splide-slide>
            <img src="~/static/images/felix-3.png" alt="Зайка" />
          </splide-slide>
           <splide-slide>
            <img src="~/static/images/felix-4.jpg" alt="Зайка" />
          </splide-slide>
           <splide-slide>
            <img src="~/static/images/felix-5.jpg" alt="Зайка" />
          </splide-slide>
           <splide-slide>
            <img src="~/static/images/felix-6.jpg" alt="Зайка" />
          </splide-slide>
           <splide-slide>
            <img src="~/static/images/felix-7.jpg" alt="Зайка" />
          </splide-slide>
           <splide-slide>
            <img src="~/static/images/felix-8.jpg" alt="Зайка" />
          </splide-slide>
           <splide-slide>
            <img src="~/static/images/felix-9.png" alt="Зайка" />
          </splide-slide>
            <splide-slide>
            <img src="~/static/images/felix-10.jpeg" alt="Зайка" />
          </splide-slide>
            <splide-slide>
            <img src="~/static/images/felix-11.jpg" alt="Зайка" />
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
        perPage: 5,
        perMove: 1,
        arrows: true,
        autoWidth: true,
        gap: 20,
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.photos {
  min-height: 1000px;
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
  border: 3px solid #ee8695;
  -webkit-box-shadow: 0px 6px 24px 3px rgba(41, 40, 49, 0.7);
  -moz-box-shadow: 0px 6px 24px 3px rgba(41, 40, 49, 0.7);
  box-shadow: 0px 6px 24px 3px rgba(41, 40, 49, 0.7);
  overflow: hidden;
}
img {
 width:100%;
 height: 100%;
 object-fit:cover;
}
</style>
