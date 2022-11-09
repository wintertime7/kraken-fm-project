<script>
  export default {
    name: "AboutMeComponent",
    data() {
      return {
        user: {
          name: "Rainers",
          surname: "Smolenskis",
          code: "IT20008"
        }
      }
    }
  }
</script>

<template>
  <section class="cerams">
    <h1>ABOUT ME</h1>
    <ul>
      <li><h3><span class="key">Name: </span>{{user.name}}</h3></li>
      <li><h3><span class="key">Surname: </span>{{user.surname}}</h3></li>
      <li><h3><span class="key">Code: </span>{{user.code}}</h3></li>
    </ul>
  </section>
</template>

<style scoped>
  ul {
    list-style: none;
  }

  h1, h3 {
    color: var(--white-color);
    font-family: 'Poppins', sans-serif;
  }

  h1 {
    font-size: 24px;
    font-weight: 900;
    margin-bottom: 25px;
  }

  h3 {
    font-weight: 500;
  }

  .key {
    font-weight: 100;
    font-style: italic;
  }

</style>