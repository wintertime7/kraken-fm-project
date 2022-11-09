<script>
  import Button from './Button.vue';

  export default {
    name: 'HeaderComponent',
    components: {
      Button
    },
    data() {
      return {
        //pls change this after testing u idiot
        show: false,
        user: {
          name: "Rainers",
          surname: "Smolenskis",
          code: "IT20008"
        }
      }
    },
    methods: {
      getFullName(name, surname) {
        let full_name = name + " " + surname;
        return full_name;
      }
    }
  }

  

</script>

<template>
  <div v-bind:class="{'nav-bar': this.show == false, 'nav-bar-active': this.show}">
    <div class="nav-logo">
      <img src="../assets/logo-white.svg">
      <h1>KRAKEN.FM</h1>
    </div>
    <div v-if="show" class="account">
      <span class="dot"></span>
      <p class="user-name">{{getFullName(user.name, user.surname)}}</p>
    </div>
    <Button />
  </div>
</template>

<style scoped>
  .nav-bar {
    background-color: var(--gray-color);
    display: flex;
    justify-content: flex-end;
    align-items: center;
    height: 70px;
    border-bottom: 2px var(--purple-color) solid;
  }

  .nav-bar-active {
    background-color: var(--purple-color);
    display: flex;
    justify-content: flex-end;
    align-items: center;
    height: 70px;
    border-bottom: 2px var(--purple-color) solid;
  }

  .nav-logo {
    margin-right: auto;
    display: flex;
    align-items: center;
    margin-left: 40px;
  }

  .nav-logo img {
    width: 50px;
    cursor: pointer;
  }

  .nav-logo h1 {
    color: var(--white-color);
    font-family: 'Poppins', sans-serif;
    font-size: 22px;
    cursor: pointer;
  }

  .account {
    height: 35px;
    display: flex;
    align-items: center;
    margin-right: 7px;
    border-right: 2px white solid;
  }

  .user-name {
    color: var(--white-color);
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
    font-size: 16px;
    margin-right: 7px;
  }

.dot {
  height: 33px;
  width: 33px;
  background-color: rgb(212, 212, 212);
  border-radius: 50%;
  display: inline-block;
  margin-right: 7px;
  border: 2px var(--white-color) solid;
}

</style>