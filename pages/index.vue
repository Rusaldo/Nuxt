<template>
  <div>
    <HeroSection />
    <ServicesSection />
    <FeaturesSection />
<!--    <HowMuchSection />-->
    <ApplySection />
  </div>
</template>

<script>
import HeroSection from '~/components/HeroSection.vue'
import FeaturesSection from '~/components/FeaturesSection.vue'
import HowMuchSection from '~/components/HowMuchSection.vue'
import ServicesSection from '~/components/ServicesSection.vue'
import ApplySection from '~/components/ApplySection.vue'

export default {
  components: {
    HeroSection,
    FeaturesSection,
    HowMuchSection,
    ServicesSection,
    ApplySection
  }
}
</script>
