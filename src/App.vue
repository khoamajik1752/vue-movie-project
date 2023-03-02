<template>
    <div>
        <VueHeader :darkMode="darkMode"  :apiKey="apiKey" @switchmode="updatemode($event)"/>
        <VueNav></VueNav>
        <VueTopMovie></VueTopMovie>
        <VueMainRate></VueMainRate>        
        <vueN />
        <component  :is="currentTab" :theaterList="theaterList" :popularList="popularList" :apiKey="apiKey" :id="id"  :ratingList="ratingList" @swap="swap($event)" ></component>
        <vueH :darkMode="false" :apiKey="apiKey" @switchmode="updatemode($event)"/>
    </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import VueHeader from './components/HeaderComponent.vue'
import VueNav from './components/NavBarComponent.vue'
import VueTopMovie from './components/TopMovieComponent.vue'
import VueMainRate from './components/MainRatingComponent.vue'
export default {
  data () {
    return {
    }
  },
  methods: {
  },
  name: 'App',
  components: {
    HelloWorld,
    VueHeader,
    VueNav,
    VueTopMovie,
    VueMainRate
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
  
}
</style>
