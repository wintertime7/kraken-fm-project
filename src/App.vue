<script>
  import HeaderComponent from './components/HeaderComponent.vue';
  import BodyComponent from './components/BodyComponent.vue';

  export default {
    name: 'App',
    components: {
      HeaderComponent,
      BodyComponent
    },
    data() {
      return {
        show: false
      }
    }
  }
</script>

<template>
  <HeaderComponent/>
  <BodyComponent v-if="show" />
</template>

<style></style>