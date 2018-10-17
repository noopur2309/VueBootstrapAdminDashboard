<template>
<div>
 <div class="panel panel-headline">
                            <div class="panel-heading">
                               <h3 class="panel-subtitle" v-text="panelsubTitle"></h3>
                            </div>
                            <div class="panel-body">
                                <div class="row">
                                    <div class="col-md-6">
                                        <div class="panel">
                                        <div class="panel-heading">
                                        <h3 class="panel-title" v-text="paneltitle"></h3>
                                        <h3 class="panel-title"></h3>

                                    </div>
                                   
	                                <VueChart type="horizontalBar" :data="datacollection" :options="options"></VueChart>
<!--	                                 <canvas id="myBarChart1"></canvas>-->
                                          
                                
                                    </div>
                                    </div>

                                    <div class="col-md-6">
                                       <div class="panel">
                                        <div class="panel-heading">
                                         <h3 class="panel-title" v-text="panel"></h3>
                                        
                                   </div>
                                            <VueChart type="doughnut" :data="datapie"></VueChart>
<!--                                         <canvas id="myDoughnutChart1"></canvas>-->
                                        </div>
                                    </div>
                                    
                               </div> <!-- First Row-->
                            </div>
                        </div> <!-- First Panel-->
    
    
    
</div>
</template>
<script>
  import  tabgraph from './tabgraph.vue'
  import VueChart from 'vue-chart-js'
  
    
    export default{
        
        components:{
            tabgraph,
            VueChart
        
          },
        data (){
             return {
                 panelsubTitle:'Network Map',
                 paneltitle:'Typical Power And Total Power',
                 panel:'NetworkWise Wavelength Used',
			     datacollection: {
                 labels: ["1", "2", "3" ,"4" ,"5" ,"6" ,"7" ,"8"],
                 datasets: [
                     {
                  label: 'Total Power',
                  backgroundColor: "#880e4f",
                 data:[2000,4000,1000,4500,3000,6000,8000,5000],
                     stack:1
                 },
                     
                    {
                    label:'Power Consumption',
                     backgroundColor:"#ff6b6d",
                     data:[1000,1500,3500,7000,6500,3000,7500,2000],
                     stack:1,

                }, 
                      ]

              }, 
                  options:{ 
                           legend: {
                                display: true
                             },
//                         
                            tooltips: {
                                mode: "single",
                                    intersect: true
                            },
                            hover: {
                                mode: 'nearest',
                                intersect: true
                            },
                            scales: {
                                xAxes: [{
                                    display: true,
                                    stacked: true,
                                    scrollbar: {
                                         enabled: true
                                     },
                                    scaleLabel: {
                                        display: true,

                                        labelString: 'Power(Watt)'
                                    }
                                }],
                                yAxes: [{
                                    display: true,
                                    scaleLabel: {
                                        display: true,
                                        stacked: true,

                                        labelString: 'Node Id'

                                    }
                                }]
                            }
                 
                   },
                 
                 // Doughnut Chart data
                 
                datapie:{ 
                    labels: ["1","2","3","4","5","6"],
               datasets: [
                 {
                data: [40,39,41,38,43,37],
                backgroundColor: [ "#e91e63","#63FF84","#37474F","#4527a0","#4a148c"]
            }],
               }
                 
                 
//                 return end
		
		}
                 
		
		}
	
    }

  
    
    
</script>                                        
