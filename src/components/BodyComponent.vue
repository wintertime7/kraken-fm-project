<script>
  import NavButton from './NavButton.vue';
  import HomeComponent from './HomeComponent.vue';
  import AboutMeComponent from './AboutMeComponent.vue';

  export default {
    name: "BodyComponent",
    components: {
      NavButton,
      HomeComponent,
      AboutMeComponent
    },
    data() {
      return {
        showHome: true,
        showAbout: false
      }
    }
  }
</script>

<template>
  <section class="body">
    <section class="navigation">
      <NavButton text="HOME" :active="this.showHome"/>
      <NavButton text="ABOUT ME" :active="this.showAbout"/>
    </section>
    <section class="element-area">
      <HomeComponent v-if="showHome" />
      <AboutMeComponent v-if="showAbout" />
    </section>
  </section>
</template>

<style scoped>
  .body {
    display: flex;
    margin: 30px 30px 0 30px
  }

  .navigation {
    flex: 2;
    display: flex;
    flex-direction: column;
  }

  .element-area {
    display: flex;
    flex: 6;
  }
</style>