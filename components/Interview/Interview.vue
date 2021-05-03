<template>
  <div class="wrapper">
    <div class="interviews">
      <div class="interview">
        <div class="text">
          <h3>[Pops in Seoul] What is Felix(필릭스,Stray Kids)'s TMI?</h3>
        </div>
        <iframe
          src="https://www.youtube.com/embed/SmFWQl1n1V8"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
      <div class="interview">
        <div class="text">
          <h3>
            Stray Kids Talk Double Knot (English Version), District 9 Tour,
            Being a Stray Kid
          </h3>
        </div>
        <iframe
          src="https://www.youtube.com/embed/TPGJgpWWvJE"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        ></iframe>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.interviews {
  margin-bottom: 50px;
}
.interview {
  margin-top: 50px;
  width: 100%;
  text-align: center;
}
.text{
  width: max-content;
  margin: 0 auto 30px;
  background-color: #333f58;
  padding: 10px 20px;
  border-radius: 8px;
}
h3 {



  font-size: 32px;
  color: #ee8695;
}
iframe {
  border: 3px solid #333f58;
  border-radius: 8px;
  width: 80%;
  aspect-ratio: 16/9;
}
</style>
