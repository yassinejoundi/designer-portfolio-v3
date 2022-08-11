<template>
  <div class="home">
    <Hero />
    <Services />
    <About />
    <Portfolio />
  </div>
</template>

<script>
import Hero from '~/components/Hero'
import Services from '../components/Services'
import About from '~/components/About'
import Portfolio from '~/components/Portfolio'

export default {
  name: 'IndexPage',
  components: { Hero, Services, About, Portfolio },
}
</script>
