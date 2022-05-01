<template>
  <main>
    <router-view/>
    <!-- <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav> -->
  </main>  
</template>

<script>


export default {
  
}
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: "Rubik", sans-serif;
  }

  a, a:hover {
    text-decoration: none;
  }

  main{
    width: 100%;
    overflow: hidden;
  }

</style>
