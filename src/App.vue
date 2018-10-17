<template>
  <div id="app">
 <navbarComponent></navbarComponent>
       <navComponent></navComponent>
 <dashboardComponent v-for="card in 1">
    </dashboardComponent> 
<tabgraphComponent></tabgraphComponent>
<tabnameComponent></tabnameComponent>

       
  
   
   
      
      
</div>

</template>


<script>
import cardComponent from './components/card'
import dashboardComponent from './components/dashboard'
import navbarComponent from './components/navbar'
import chartComponent from './components/chart'
import searchComponent from './components/search'
import contactComponent from './components/contact'    
import navComponent from './components/nav'
import barComponent from './components/bar'
import GoogleMapComponent from './components/GoogleMap'  
import tabgraphComponent from './components/tabgraph'    
import tabnameComponent from './components/tabname'    
import bootstrap from './assets/vendor/bootstrap/css/bootstrap.min.css'
import awesome from './assets/vendor/font-awesome/css/font-awesome.min.css'
import jquery from './assets/vendor/jquery/jquery.min.js'
import bootstrapjs from './assets/vendor/bootstrap/js/bootstrap.min.js'
import VueChart from 'vue-chart-js'

export default {
  name: 'App',
  components: {
    cardComponent,
      dashboardComponent,
      navbarComponent,
      navComponent,
      chartComponent,
      searchComponent,
      contactComponent,
      barComponent,
      GoogleMapComponent,
      VueChart,
      tabgraphComponent,
      tabnameComponent
      
  }
}
</script>

<style>
#app {
   font-family: 'Avenir', Helvetica, Arial, sans-serif;
   -webkit-font-smoothing: antialiased;
   -moz-osx-font-smoothing: grayscale;
   text-align: center;
    color: #2c3e50;
    margin-top: 60px;
    width:1170px;
    padding-right: 10px;
    padding-left: 10px;
    margin-right: auto;
    margin-left: auto;
}
 
</style>
