<template>   
    <h1 class="text-3xl font-extrabold uppercase flex justify-center mt-6">Account Settings</h1>           
    <Appmain />
</template>

<script>
import Appmain from './components/Appmain';
export default {
  el: '#app',
  mounted() {
    if (localStorage.name) {
      this.name = localStorage.name;
    }
    if (localStorage.age) {
      this.age = localStorage.age;
    }
  },
  methods: {
    persist() {
      localStorage.name = this.name;
      localStorage.age = this.age;
      console.log('maintenant prétendre que j\'ai fait plus de choses...');
    }
  },

  name: 'App',
  components: { Appmain },
  
}
</script>

<style lang="scss">
h1 {
  color: #Fe2336;
}
</style>
