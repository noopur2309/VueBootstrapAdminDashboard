<template>
<div>
    <div class="row">
                            <div class="col-md-12">
                                    <div class="panel">
                                    <div class="panel-heading">
                                       
                                        <h3 class="panel-title" v-text="paneltitle"></h3>
                                    </div>
                                    <div class="panel-body" >
<!--                                    <canvas id="myChart1"></canvas>-->
                                         <VueChart type="bar" :data="databar" :options="optbar"></VueChart>
                                    </div>
                                </div>


                        </div>
                    </div>
</div>
</template>
<script>
  import  bar  from './bar.vue'
  import VueChart from 'vue-chart-js'
  
    
    export default{
        components:{
            bar,
            VueChart
       
           
        },
        data (){
             return {
                 paneltitle:'NetworkWise Price Distribution',
        databar: {
                  labels: ["1", "2", "3" ,"4" ,"5" ,"6" ,"7" ,"8"],
                 datasets: [{
                  label: 'Total Price',
                  backgroundColor: "#880e4f",
                 data:[12,19,20,35,41,12,40,15],
                 
                }, 
                      ]

              }, 

                   optbar: {
                            legend: {
                                display: true
                             },
                           
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
                                   scrollbar: {
                                         enabled: true
                                     },
                                    scaleLabel: {
                                        display: true,
                                   labelString: 'Total Network'
                                    }
                                }],
                                yAxes: [{
                                    display: true,
                                    scaleLabel: {
                                        display: true,
                                      labelString: 'Total Price($)'

                                    }
                                }]
                            },
                             responsive: true,
				maintainAspectRatio: true,
			
                        
                        }

            
            }
        }
       
    }
  
    
    
</script>                                        
