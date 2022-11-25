<script>

  import QualitySection from './QualitySection.vue';
  import SignUpSection from './SignUpSection.vue';
  import ReviewSection from './ReviewSection.vue';
  import ServicesSection from './ServicesSection.vue';
  import FacilitiesSection from './FacilitiesSection.vue';

  export default{
    name: 'AppMain',
    components:{
      QualitySection,
      SignUpSection,
      ServicesSection,
      ReviewSection,
      FacilitiesSection
    }
  }
</script>

<template>
  <main>
    <QualitySection/>

    <SignUpSection/>

    <ServicesSection/>

    <ReviewSection/>

    <FacilitiesSection/>
  </main>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
</style>