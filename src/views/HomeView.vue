<template>
  <header>
    <HomeNav />      
  </header>

  <MainCard />

  <section class="secBlock">
    <Skills />
    <Studies />
  </section>

  <Experience />

  <Projects />
  
  <Contact />

</template>

<script>
import HomeNav from '@/components/HomeNav.vue';
import MainCard from '@/components/MainCard.vue';
import Skills from '@/components/Skills.vue';
import Studies from '@/components/Studies.vue';
import Experience from '@/components/Experience.vue';
import Projects from '@/components/Projects.vue';
import Contact from '@/components/Contact.vue';

export default {
  name: 'HomeView',
  components: {
    HomeNav,
    MainCard,
    Skills,
    Studies,
    Experience,
    Projects,
    Contact
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