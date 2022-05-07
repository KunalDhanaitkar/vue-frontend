<template>

  <div class="container">

      <AppHeader pageTitle="Welcome to STUDY RESOURCES" 
        pageDesc='One stop solution for all your STUDENT needs'/>

      <ResourceBox :resources="resources"/>
      
      <v-footer>
        <AppFooter/>
      </v-footer>

  </div>

</template>

<script>

import AppHeader from './components/AppHeader.vue'
import ResourceBox from './components/ResourceBox.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    ResourceBox,
    AppFooter
},

  data(){
    return{
      resources: []
    }
  },

  methods: {

    async fetchResources(){
      const res = await fetch("https://kunaldhanaitkar.herokuapp.com/api/resources");
      const data = await res.json()

      return data
    }

  },

  async created(){
    this.resources = await this.fetchResources()
  }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body{
  font-family: 'Montserrat', sans-serif;
}

.container{
  max-width: 1800px;
  margin: 30px auto;
  overflow: auto;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
  background-color: white(0, 0, 0);
}

div{
  margin-bottom: 0.5em;
}

</style>
