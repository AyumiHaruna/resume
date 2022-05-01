<template>
  <header>
    <HomeNav />      
  </header>

  <MainCard />
</template>

<script>
import HomeNav from '@/components/HomeNav.vue';
import MainCard from '@/components/MainCard.vue';

export default {
  name: 'HomeView',
  components: {
    HomeNav,
    MainCard
  },
}
</script>

<style>

</style>