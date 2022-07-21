<template>
  <nav>
    <ul>
      <li><a href="#">HOME</a></li>
      <li><a href="#">ABOUT</a></li>
      <li><a href="#">SERVICES</a></li>
      <li><a href="#">HELP?</a></li>
    </ul>
  </nav>
</template>

<script>
export default {

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  * {
    margin: 0;
    padding: 0;
  }
  nav {
    background: rgb(180, 31, 31);
    margin: 0;
    padding: 5px;
  }
  ul {
    display: flex;
  }
  li {
    list-style: none;
    padding: 10px 20px;
  }
  a {
    color: #fff;
    text-decoration: none;
  }
</style>
