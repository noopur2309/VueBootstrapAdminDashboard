<template>
<div>
         <div class="row">
         <div class="col-md-12">
                            <!-- contact us -->
     <div class="panel">
        <div class="panel-heading">
      <h3 class="panel-title" v-text="paneltitle"></h3>
<gmap-map
    :center="center"
    :zoom="7"
    style="width: 1100px; height: 300px"
  >
    <gmap-marker
      :key="index"
      v-for="(m, index) in markers"
      :position="m.position"
      :clickable="true"
      :draggable="true"
      @click="center=m.position"
    ></gmap-marker>
  </gmap-map>
             
        </div>
         </div>
                    </div>
                    </div>
</div>
</template>
<script>
  import GoogleMap from './GoogleMap.vue'
     import  VueGoogleMaps from 'vue2-google-maps'
  
    
    export default{
        components:{
            GoogleMap,
            VueGoogleMaps
           },
       
  
    data () {
      return {
        center: {lat:28.7041, lng: 77.1025},
        markers: [{
          position: {lat:23.033863, lng:72.585022}
        }, {
          position: {lat:12.9716, lng:77.5946}
        }]
      }
    }
  }
        
       

  
    
    
</script>     