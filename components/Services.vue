<template>
  <div id="services" class="services">
    <h1 class="section-title">Serv<span>i</span>ces</h1>
    <div class="service-bottom">
      <div class="service-item" v-for="service in services" :key="service.id">
        <div class="icon">
          <img :src="require(`@/static/img/${service.icon}-icon.svg`)" />
        </div>
        <h2>{{ service.title }}</h2>
        <p>{{ service.content }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      services: [
        {
          title: 'Graphic Design',
          icon: 'stationery',
          content:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis debitis rerum, magni voluptatem sed architecto placeat beatae tenetur officia quod',
        },
        {
          title: 'Social Postes',
          icon: 'brochure-catalog',
          content:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis debitis rerum, magni voluptatem sed architecto placeat beatae tenetur officia quod',
        },
        {
          title: 'Brand Identity',
          icon: 'brand-identity',
          content:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis debitis rerum, magni voluptatem sed architecto placeat beatae tenetur officia quod',
        },
      ],
    }
  },
}
</script>

<style scoped>
.services {
  text-align: center;
  padding: 100px 0;
}

.service-bottom {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  gap: 30px;
  margin-top: 50px;
}
.service-item {
  width: max(300px, 25%);
  display: flex;
  align-items: flex-start;
  justify-content: center;
  flex-direction: column;
  padding: 30px;
  border-radius: 10px;
  background-image: url(@/static/img/img-1.png);
  background-size: cover;
  position: relative;
  z-index: 1;
  overflow: hidden;
}
.service-item::after {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  height: 100%;
  width: 100%;
  background-image: linear-gradient(
    60deg,
    rgba(28, 56, 121, 1) 0%,
    rgba(96, 126, 170, 1) 100%
  );
  opacity: 0.9;
  z-index: -1;
}
.icon {
  width: 100%;
  margin-bottom: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.icon img {
  width: 100px;
  height: 100px;
}
.service-item h2 {
  font-size: 2rem;
  color: white;
  margin-bottom: 10px;
  text-transform: uppercase;
  text-align: center;
}
.service-item p {
  color: white;
  text-align: left;
}
</style>
