<script>

  import QualitySection from './QualitySection.vue';
  import SignUpSection from './SignUpSection.vue';
  import ReviewSection from './ReviewSection.vue';
  import ServicesSection from './ServicesSection.vue';

  export default{
    name: 'AppMain',
    components:{
      QualitySection,
      SignUpSection,
      ServicesSection,
      ReviewSection
    }
  }
</script>

<template>
  <main>
    <QualitySection/>

    <SignUpSection/>

    <ServicesSection/>

    <ReviewSection/>
  </main>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
</style>