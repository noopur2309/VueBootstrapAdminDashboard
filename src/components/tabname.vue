<template>
<div>
   <div class="panel panel-headline"> 
                            <div class="panel-heading">
                             <h3 class="panel-subtitle" v-text="panelsubTitle"></h3>
                         </div>
                            <div class="panel-body">
                                <div class="row">
                                      <div class="col-md-6">
                                      <div class="statistics">
                  <div class="statistic d-flex align-items-center bg-white has-shadow">
                    <div class="icon bg-red"><i class="glyphicon glyphicon-tasks"></i></div>
                    <div class="text"><strong v-text="wavenum"></strong><br><small v-text="wavelength"></small></div>
                  </div>
                  <div class="statistic d-flex align-items-center bg-white has-shadow">
                    <div class="icon bg-green"><i class="glyphicon glyphicon-calendar"></i></div>
                    <div class="text"><strong v-text="totalcost"></strong><br><small v-text="cost"></small></div>
                  </div>
                  <div class="statistic d-flex align-items-center bg-white has-shadow">
                    <div class="icon bg-orange"><i class="glyphicon glyphicon-forward"></i></div>
                    <div class="text"><strong v-text="etc"></strong><br><small v-text="etcname"></small></div>
                  </div>
                </div>   
                                    </div>      
                                          <div class="col-md-6">
                                            <div class="col-md-12">
                                                 <div class="col-md-6">
                                                <div class="well well-sm">
                                                   <i class="glyphicon glyphicon-folder-open m-b-5 font-16"></i>
                                                   <h5 class="m-b-0 m-t-5" v-text="network"></h5>
                                                   <small class="font-light" v-text="networkname"></small>
                                                </div>
                                            </div>
                                            <div class="col-md-6">
                                                <div class="well well-sm">
                                                   <i class="fa fa-table m-b-5 font-16"></i>
                                                   <h5 class="m-b-0 m-t-5" v-text="mess"></h5>
                                                   <small class="font-light" v-text="topologyname"></small>
                                                </div>
                                            </div>
                                                 </div>
                                                 
                                                      <div class="col-md-12"> 
                                            <div class="col-md-4">
                                                <div class="well">
                                                   <i class="glyphicon glyphicon-user m-b-5 font-16"></i>
                                                   <h5 class="m-b-0 m-t-5" v-text="node"></h5>
                                                   <small class="font-light" v-text="nodename"></small>
                                                </div>
                                            </div>
                                             <div class="col-md-4">
                                                <div class="well">
                                                   <i class="glyphicon glyphicon-menu-hamburger m-b-5 font-16"></i>
                                                   <h5 class="m-b-0 m-t-5" v-text="link"></h5>
                                                   <small class="font-light" v-text=linkname></small>
                                                </div>
                                            </div>
                                            <div class="col-md-4">
                                                <div class="well">
                                                   <i class="glyphicon glyphicon-signal m-b-5 font-16"></i>
                                                   <h5 class="m-b-0 m-t-5" v-text="length"></h5>
                                                   <small class="font-light" v-text="lengthname"></small>
                                                </div>
                                            </div>
                                                
                                            </div>
                                    </div>
                                     
                                      
                                
                          
                                   
                                
                       </div> <!-- Second Row-->
                            
                            
                            
                            
                            </div>
                            </div> <!-- Second Panel-->
                            
                            
                            
                            
                   
</div>
</template>
<script>

    

    
 import tabname from './tabname.vue'

    export default{
        components:{
           tabname
            
          
        
        },
        data (){
             return {
                 panelsubTitle:'Network Details',
                 network:'SAMPLE',
                 mess:'MESS',
                 node:'12',
                 link:'4',
                 length:'1040',
                 lengthname:'Span Length',
                 linkname:'Links',
                 nodename:'Nodes',
                 topologyname:'Topology',
                 networkname:'Network',
                 wavenum:'121',
                 totalcost:'1552',
                 etc:'147',
                 wavelength:'Total Wavelengths',
                 cost:'Total costs',
                 etcname:'etc'
                 
                 

                
            }
        }
      
    }
  
    
    
</script>          