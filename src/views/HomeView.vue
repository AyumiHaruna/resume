<template>
  <header>
    <HomeNav />      
  </header>

  <MainCard />

  <section class="secBlock">
    <Skills />
    <Studies />
  </section>

  <section style="background:#220136; height: 20em; z-index:2;"></section>
</template>

<script>
import HomeNav from '@/components/HomeNav.vue';
import MainCard from '@/components/MainCard.vue';
import Skills from '@/components/Skills.vue';
import Studies from '@/components/Studies.vue';

import 'animate.css';


export default {
  name: 'HomeView',
  components: {
    HomeNav,
    MainCard,
    Skills,
    Studies
  },
}
</script>

<style scoped>
  .secBlock{
    display:flex;
    flex-direction: row;
    justify-content: space-evenly;
    flex-wrap: wrap;
  }
</style>