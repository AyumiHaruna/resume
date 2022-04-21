<template>
  <main>
    <header>
      <Navbar />
    </header>

    <section>
      <router-view/>
    </section>


    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
  </main>  
</template>

<script>
import Navbar from '@/components/Navbar.vue';

export default {
  components: {
    Navbar
  },
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
</style>
