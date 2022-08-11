<template>
  <div class="portfolio" id="portfolio">
    <h1 class="section-title">Recent <span>Projects</span></h1>
    <div class="gallery">
      <img
        v-for="i in 9"
        :key="i"
        :src="require(`@/static/img/gallery/gallery-${i}.jpg`)"
      />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.gallery {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
  padding: 20px;
  background: linear-gradient(
      45deg,
      rgba(28, 56, 121, 0.9),
      rgba(156, 158, 254, 0.9),
      rgba(171, 201, 255, 0.9),
      rgba(58, 180, 242, 0.9),
      rgba(96, 126, 170, 0.9)
    )
    0 0 / 1000% no-repeat;
  -webkit-animation: gradientAnimation 40s ease infinite; /*in the style.css*/
  animation: gradientAnimation 40s ease infinite; /*in the style.css*/
}
.gallery img {
  width: 335px;
  height: 450px;
  transition: 0.3s ease transform;
}

.gallery img:hover {
  transform: scale(1.05);
}
</style>
