<template>
<div>
 
        
              <div class="col-md-3">

            <div class="card  green-field-card">
                    <img v-bind:src="image1" class="card-img-top img-responsive"  alt="Network">
                   <a>
                 <div class="mask rgba-white-slight"></div>
                </a>

            <!-- Card content -->
            <div class="card-body card-body-cascade text-center">

            <!-- Title -->
                
      
            <a v-text="TheNetworkName" href="#" class="btn btn-success"></a>

   
<!--            <a type="button" class="btn btn-primary" @click="openNewTab">New tab</a>-->
           
                
     
    
          <br>
            <a v-on:click="handleClick('test')" href="#" class="OpenMap" title="OpenMap" data-toggle="tooltip"><i class="glyphicon glyphicon-eye-open"> </i></a>
            <a v-on:click="handleClick('second')" href="#" class="Clone" title="Clone" data-toggle="tooltip"><i class="glyphicon glyphicon-pencil"> </i></a>
            <a v-on:click="handleClick('delete')" href="#" class="Delete" title="Delete" data-toggle="tooltip"><i class="glyphicon glyphicon-trash"> </i></a>
            </div>
            </div>
            </div>
    
                               
</div>



</template>
       


                                        
                                        
<script>
  import  card  from './card.vue'
  import  nav  from './nav.vue'
  
  
    
    export default{
        components:{
            card,
            nav
       
           
        },
        data (){
             return {
                 image1:require("./../assets/MeshTopology.png"),
                 TheNetworkName:'Network',
             }
        }
  
    }
    
</script>                                        
