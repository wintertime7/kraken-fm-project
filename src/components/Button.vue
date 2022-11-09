<script>
  export default {
    name: "Button",
    data() {
      return {
        text: "LOGIN"
      }
    },
    methods: {
      toggleText() {
        if (this.$parent.show == false) {
          this.text = "LOGOUT";
          this.$parent.show = true;
        } else {
          this.text = "LOGIN";
          this.$parent.show = false;
        }
      }
    }
  }
</script>

<template>
  <button @click="toggleText" v-bind:class="{'log-btn': this.$parent.show == false, 'log-btn-clicked': this.$parent.show}">{{text}}</button>
</template>

<style scoped>
  .log-btn {
    background-color: var(--purple-color);
    padding: 5px 16px;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    transition: all 0.3s ease 0s;
    color: var(--white-color);
    font-family: 'Poppins', sans-serif;
    font-weight: 700;
    margin-right: 40px;
  }

  .log-btn:hover {
    background-color: var(--purple-hover);
  }

  .log-btn-clicked {
    background-color: rgb(9, 9, 9);
    padding: 5px 16px;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    transition: all 0.3s ease 0s;
    color: var(--white-color);
    font-family: 'Poppins', sans-serif;
    font-weight: 700;
    margin-right: 40px;
  }

  .log-btn-clicked:hover {
    background-color: var(--purple-hover);
  }

</style>