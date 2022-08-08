<template>
  <div class="home">
    <Hero />
    <Services />
    <About />
  </div>
</template>

<script>
import Hero from '~/components/Hero'
import Services from '../components/Services'
import About from '~/components/About'

export default {
  name: 'IndexPage',
  components: { Hero, Services, About },
}
</script>
