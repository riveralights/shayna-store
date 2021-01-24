<template>
  <div class="home">
    <HeaderShayna/>
    <HeroShayna/>
    <SliderShayna/>
    <InstaShayna/>
    <LogoPartner/>
    <FooterShayna/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderShayna from '@/components/HeaderShayna.vue'
import HeroShayna from '@/components/HeroShayna.vue'
import SliderShayna from '@/components/SliderShayna.vue'
import InstaShayna from '@/components/InstaShayna.vue'
import LogoPartner from '@/components/LogoPartner.vue'
import FooterShayna from '@/components/FooterShayna.vue'

export default {
  name: 'Home',
  components: {
    HeaderShayna,
    HeroShayna,
    SliderShayna,
    InstaShayna,
    LogoPartner,
    FooterShayna,
  }
}
</script>
