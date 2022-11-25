<script>

  import QualitySection from './QualitySection.vue';
  import SignUpSection from './SignUpSection.vue';

  export default{
    name: 'AppMain',
    components:{
      QualitySection,
      SignUpSection
    }
  }
</script>

<template>
  <main>
    <QualitySection/>

    <SignUpSection/>
  </main>
</template>

<style lang="scss" scoped>
  @use '../styles/partials/vars' as *;
  @use '../styles/partials/mixin' as *;
</style>