<template>
  <div id="services" class="services">
    <h1 class="section-title">Serv<span>i</span>ces</h1>
    <div class="service-bottom">
      <div class="service-item" v-for="service in services" :key="service.id">
        <div class="icon">
          <img :src="service.icon" />
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
          title: 'Graphic design',
          icon: 'https://img.icons8.com/bubbles/100/000000/services.png',
          content:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis debitis rerum, magni voluptatem sed architecto placeat beatae tenetur officia quod',
        },
        {
          title: 'Graphic design',
          icon: 'https://img.icons8.com/bubbles/100/000000/services.png',
          content:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis debitis rerum, magni voluptatem sed architecto placeat beatae tenetur officia quod',
        },
        {
          title: 'Graphic design',
          icon: 'https://img.icons8.com/bubbles/100/000000/services.png',
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
.service-bottom .icon {
  height: 120px;
  width: 120px;
  margin-bottom: 20px;
}
.service-item h2 {
  font-size: 2rem;
  color: white;
  margin-bottom: 10px;
  text-transform: uppercase;
}
.service-item p {
  color: white;
  text-align: left;
}
</style>
