<script>

  import QualitySection from './QualitySection.vue';
  import SignUpSection from './SignUpSection.vue';
  import ReviewSection from './ReviewSection.vue';
  import ServicesSection from './ServicesSection.vue';
  import FacilitiesSection from './FacilitiesSection.vue';
  import QuoteSection from './QuoteSection.vue';
  import TrainersSection from './TrainersSection.vue';
  import PerformanceNewsSection from './PerformanceNewsSection.vue';
  import JoinSection from './JoinSection.vue';

  export default{
    name: 'AppMain',
    components:{
      QualitySection,
      SignUpSection,
      ServicesSection,
      ReviewSection,
      FacilitiesSection,
      QuoteSection,
      TrainersSection,
      PerformanceNewsSection,
      JoinSection
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

    <QuoteSection/>

    <TrainersSection/>

    <PerformanceNewsSection/>

    <JoinSection/>
  </main>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
</style>