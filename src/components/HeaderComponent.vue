<script>
  export default {

  }
</script>

<template>
  <div class="nav-bar">
    <div class="nav-logo">
      <img src="../assets/logo-white.svg">
      <h1>KRAKEN.FM</h1>
    </div>
    <button class="log-btn">LOGIN</button>
  </div>
</template>

<style scoped>
  .nav-bar {
    background-color: var(--gray-color);
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 70px;
    border-bottom: 2px var(--purple-color) solid;
  }

  .nav-logo {
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

</style>