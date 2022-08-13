<template>
  <div id="foot" class="foot">
    <p class="get-designs">Let Me Get You A Beautiful Designs</p>
    <div class="foot-info">
      <div class="phone">
        <a :href="`tel:${phone}`">
          <i class="mdi mdi-phone"></i>
          Phone: {{ phone }}
        </a>
      </div>
      <div class="email">
        <a :href="`mailto:${email}`">
          <i class="mdi mdi-send"></i>
          Email: {{ email }}
        </a>
      </div>
      <div class="social">
        <a v-for="social in socials" :key="social.id" :href="social.link">
          <i :class="`mdi mdi-${social.icon}`"></i>
        </a>
      </div>
    </div>
    <p class="end">
      © 2022 CopyRight By
      <a href="https://www.linkedin.com/in/yassinejoundi">Joundi Yassine</a>
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: this.$store.state.data.name,
      socials: this.$store.state.data.socials,
      phone: '+212612345789',
      email: 'contact@email.com',
    }
  },
}
</script>

<style scoped>
.foot {
  padding: 40px 40px 10px;
}

.get-designs {
  text-align: center;
  font-size: 18px;
  font-weight: 500;
}

.foot-info {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
  flex-wrap: wrap;
  padding: 20px 0;
}

.foot-info div {
  width: 300px;
}

.phone a,
.email a {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  gap: 10px;
  cursor: pointer;
}

i {
  font-size: 30px;
  color: var(--primary-color);
}

.end {
  color: #000;
  padding: 20px;
  font-size: 18px;
  text-align: center;
}

.phone a,
.email a,
.end a {
  color: var(--primary-color);
  text-decoration: none;
  font-size: 18px;
}
</style>
