<template>
  <div class="home">
    <Hero />
    <Services />
    <About />
    <Portfolio />
    <Foot />
  </div>
</template>

<script>
import Hero from '~/components/Hero'
import Services from '../components/Services'
import About from '~/components/About'
import Portfolio from '~/components/Portfolio'
import Foot from '../components/Foot'

export default {
  name: 'IndexPage',
  components: { Hero, Services, About, Portfolio, Foot },
}
</script>
