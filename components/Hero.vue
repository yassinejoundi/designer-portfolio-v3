<template>
  <div class="hero" id="hero">
    <div class="hero-content">
      <div class="hero-img">
        <img :src="require('@/static/img/author.jpg')" :alt="name" />
      </div>
      <h1>
        <span>{{ name }}</span>
      </h1>
      <h3><span>Graphic Designer / Photographer</span></h3>
      <div class="social">
        <a v-for="social in socials" :key="social.id" :href="social.link">
          <i :class="`mdi mdi-${social.icon}`"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: this.$store.state.data.name,
      socials: this.$store.state.data.socials,
    }
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Kaushan+Script');
.hero {
  height: 100vh;
  background: linear-gradient(
        45deg,
        rgba(28, 56, 121, 0.85),
        rgba(156, 158, 254, 0.85),
        rgba(171, 201, 255, 0.85),
        rgba(58, 180, 242, 0.85),
        rgba(96, 126, 170, 0.85)
      )
      0 0 / 1000% no-repeat,
    url(@/static/img/bg-hero.jpg) 0 0 / cover no-repeat;
  -webkit-animation: gradientAnimation 40s ease infinite;
  animation: gradientAnimation 40s ease infinite;
  position: relative;
}
@-webkit-keyframes gradientAnimation {
  0% {
    background-position: 0% 30%, 0 0;
  }
  50% {
    background-position: 100% 70%, 0 0;
  }
  100% {
    background-position: 0% 30%, 0 0;
  }
}
@keyframes gradientAnimation {
  0% {
    background-position: 0% 30%, 0 0;
  }
  50% {
    background-position: 100% 70%, 0 0;
  }
  100% {
    background-position: 0% 30%, 0 0;
  }
}
.hero-content {
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  color: #fff;
  text-align: center;
  width: 100vw;
  padding: 10px;
}

.hero-img img {
  background-size: cover !important;
  background-position: center center;
  background-repeat: no-repeat;
  height: 200px;
  width: 200px;
  margin: 0 auto;
  margin-bottom: 30px;
  border-radius: 50%;
  box-shadow: 2px 3px 10px rgba(28, 56, 121, 0.7);
}

.hero-content h1 {
  margin-bottom: 30px;
  font-size: 50px;
  line-height: 1.3;
  font-weight: 300;
  -webkit-transform: rotate(-5deg);
  -moz-transform: rotate(-5deg);
  -ms-transform: rotate(-5deg);
  -o-transform: rotate(-5deg);
  transform: rotate(-5deg);
}

.hero-content h1 span {
  padding: 4px 15px;
  position: relative;
  font-family: 'Lobster', cursive !important;
}

.hero-content h1 span:before {
  position: absolute;
  top: 40px;
  left: 0;
  width: 30px;
  height: 4px;
  content: '';
  background: #fff;
  margin-left: -30px;
}

.hero-content h1 span:after {
  position: absolute;
  top: 40px;
  right: 0;
  width: 30px;
  height: 4px;
  content: '';
  background: #fff;
  margin-right: -30px;
}

.hero-content h3 {
  font-size: 18px;
}

@media screen and (max-width: 768px) {
  .hero-content h1 {
    font-size: 34px;
  }
  .hero-content h1 span:before {
    top: 28px;
    width: 20px;
    height: 3px;
    margin-left: -15px;
  }
  .hero-content h1 span:after {
    top: 28px;
    width: 20px;
    height: 3px;
    margin-right: -15px;
  }
  .hero-content h3 {
    font-size: 16px;
  }
}
</style>
