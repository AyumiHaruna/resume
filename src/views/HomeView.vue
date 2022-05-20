<template>
  <header>
    <HomeNav />      
  </header>

  <MainCard id="about" />

  <section class="secBlock">
    <Skills id="skills" />
    <Studies id="studies" />
  </section>

  <Experience id="experience" />

  <Projects id="projects" />
  
  <Contact id="contact" />

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