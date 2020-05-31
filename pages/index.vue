<template>
  <div>
    <FeaturesSection />
    <HowMuchSection />
    <ServicesSection />
    <ApplySection />
  </div>
</template>

<script>
import FeaturesSection from '~/components/FeaturesSection.vue'
import HowMuchSection from '~/components/HowMuchSection.vue'
import ServicesSection from '~/components/ServicesSection.vue'
import ApplySection from '~/components/ApplySection.vue'

export default {
  components: {
    FeaturesSection,
    HowMuchSection,
    ServicesSection,
    ApplySection
  }
}
</script>
