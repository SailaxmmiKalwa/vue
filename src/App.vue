<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <TopHero />
  <div style="margin-top: 50px;">

  </div>
  <CardsList 
    :companieslist = companiesdata
  />
</template>

<script>
import TopHero from './components/topHero.vue';
import cardComponent from './components/cardComponent.vue'
import CardsList from './components/cardsList.vue';

export default {
  mounted() {
  fetch('https://node-server-j500.onrender.com/api')
        .then(response => response.json())
        .then(data => {
          this.companiesdata = data;
        })
        .catch(error => console.error('Error fetching JSON data:', error));
  },
  name: 'App',
  components: {
    TopHero,
    cardComponent,
    CardsList
  },
  data (){
    return {
      companiesdata : [],
      data : null
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
