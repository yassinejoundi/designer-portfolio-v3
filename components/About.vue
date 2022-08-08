<template>
  <div id="about" class="about">
    <div class="main">
      <div class="about-img">
        <img :src="require('@/static/img/author.jpg')" />
      </div>
      <div class="about-text">
        <h1 class="section-title">About<span>me</span></h1>
        <h2>Graphic Designer</h2>
        <p>
          I'm a full-time graphic designer and photographer with over 10 years
          of experience. I specialize in logo design and branding, along with
          custom logos, social media graphics and print collateral such as
          business cards, flyers and brochures. I have more than 4k followers on
          Instagram and am able to grow your brand through social media
          marketing.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About',
}
</script>

<style scoped>
.about {
  padding: 100px 40px;
}

.about-img,
.about-img img {
  height: auto;
  width: 280px;
}

.about-img img {
  border: 5px solid white;
}

.about-img {
  position: relative;
}

.about-img::after {
  content: '';
  position: absolute;
  left: -25px;
  top: 10px;
  height: 98%;
  width: 98%;
  border: 7px solid var(--primary-color);
  z-index: -1;
}

.about-text {
  width: 450px;
  padding: 0 5px 0 20px;
}

.main {
  width: 90%;
  padding: 0 20px;
  display: flex;
  align-items: center;
  justify-content: space-around;
  flex-wrap: wrap-reverse;
}

.about-text h2 {
  font-size: 1.8rem;
  font-weight: 500;
  letter-spacing: 0.2rem;
  margin-bottom: 10px;
}

.about-text p {
  font-size: 1rem;
  margin-top: 5px;
  line-height: 2rem;
  font-weight: 300;
  letter-spacing: 0.05rem;
  margin-bottom: 20px;
}
</style>
