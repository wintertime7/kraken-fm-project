<script>
  export default {
    name: "NavButton",
    props: {
      text: String,
      active: Boolean
    },
    methods: {
      tests() {
        if (this.active == this.$parent.showHome) {
          this.$parent.showHome = true;
        } else {
          this.$parent.showHome = false;
        }

        if (this.active == this.$parent.showAbout) {
          this.$parent.showAbout = true;
        } else {
          this.$parent.showAbout = false;
        }
      }
    }
  }
</script>

<template>
  <button @click="tests()" v-bind:class="{'btn': this.active == false, 'btn-active': this.active}">{{text}}</button>
</template>

<style scoped>
  .btn {
    width: 85%;
    text-align: left;
    background: transparent;
    padding: 10px 0 10px 20px;
    border: none;
    cursor: pointer;
    transition: all 0.3s ease 0s;
    color: var(--white-color);
    font-family: 'Poppins', sans-serif;
    font-size: 16px;
    font-weight: 700;
  }

  .btn:hover {
    background-color: var(--purple-color);
    clip-path: polygon(100% 0, 100% 100%, 0 100%, 0 0);
  }

  .btn-active {
    width: 85%;
    text-align: left;
    background-color: var(--purple-color);
    clip-path: polygon(100% 0, 92% 100%, 0 100%, 0 0);
    padding: 10px 0 10px 20px;
    border: none;
    cursor: pointer;
    transition: all 0.3s ease 0s;
    color: var(--white-color);
    font-family: 'Poppins', sans-serif;
    font-size: 16px;
    font-weight: 700;
  }

  .btn-active:hover {
    background-color: var(--purple-color);
    clip-path: polygon(100% 0, 100% 100%, 0 100%, 0 0);
  }

</style>