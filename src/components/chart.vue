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

                                    </div>
<!--                                         <canvas :data="datacollection" :options="options"></canvas>-->
                                              <VueChart type="line" :data="datacollection" :options="options"></VueChart>
                                  
                                      
                                    </div>
                                    </div>

                                    <div class="col-md-6">
                                       <div class="panel">
                                        <div class="panel-heading">
                                        <h3 class="panel-title" v-text="panel"></h3>

                                    </div>
<!--                                         <canvas id="mypieChart"></canvas>-->
                 
                                <VueChart type="pie" :data="datapie" :options="opt"></VueChart>
                                  
                                     
                                      
 

                                    </div>
                                </div>
                            </div>
                        </div>
                            </div>  
</div>
</template>

<script>
  import  chart  from './chart.vue'
  import VueChart from 'vue-chart-js'
  
    
    export default{
        
        components:{
            chart,
            VueChart
        
          },
        data (){
             return {
                 panelsubTitle:'Network Map',
                 paneltitle:'NetworkWise Power Distribution',
                 panel:'NetworkWise Network Elements',
			     datacollection: {
				 labels: ['Network 1', 'Network 2', 'Network 3', 'Network 4', 'Network 5', 'Network 6'],
				 datasets: [
					{
						label: 'Power(db)',
						backgroundColor: '#f87979',
						pointBackgroundColor: 'white',
						borderWidth: 1,
						pointBorderColor: '#249EBF',
						data: [40, 20, 30, 50, 90, 10]
					}
]
			},
                  options:{ 
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

                                        labelString: 'Network'
                                    },gridLines: {
							display: false
						}
                                }],
                                yAxes: [{
                                    display: true,
                                    scaleLabel: {
                                        display: true,
                                      labelString: 'Power(db)'

                                    },
                                    gridLines: {
							display: true
						}
                                }]
                            },
                      responsive: true,
				maintainAspectRatio: true,
				height: 200
                        },
                 
//               pie chart data
                 datapie:{                             
                  labels: ["CDC","ILA","TE","B&S","CD-R","HUB"],
                datasets: [
                {
                backgroundColor: [ "#FF6384","#63FF84","#84FF63","#8463FF","#6384FF","#41B883"],
                data: [1, 8, 5, 5, 5,4]
                }
                ]
                },
                 opt:{
                 responsive: true, 
                 maintainAspectRatio: true,
                 }
                 
//                 return end
                 
                   }
		
		}
                 
		
		}
	


  
    
    
</script>                                        
