<template>
  <div class="home">
    <Hero />
    <Services />
  </div>
</template>

<script>
import Hero from '~/components/Hero'
import Services from '../components/Services'

export default {
  name: 'IndexPage',
  components: { Hero, Services },
}
</script>
