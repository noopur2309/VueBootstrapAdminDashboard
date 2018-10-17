<template>
<div>
    <div class="panel panel-headline">
                          <div class="panel-heading">
                            <h3 class="panel-title" v-text="dashboard"></h3>
                          <a href="#" class="pull-right">Refresh <i class="glyphicon glyphicon-refresh" aria-hidden="true"></i></a>
                                <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseOne">View All Networks</a>
                            </div>


                             <div class="scroll">
                             <div class="panel-body">
                                <div class="row">
                                    <div class="col-md-3">
                                      <div class="card">
                                             <img v-bind:src="image2" class="card-img-top img-responsive"  alt="add">
                                           <div class="card-body">
                                               <a href="#" v-show="!show" class="btn btn-success" data-toggle="modal" data-target="#myModal">Create New Network</a>
                                            <p>
    <!--					<span class="number">35%</span>-->
    <!--					<span class="title">Create New Network</span>-->
    <!--                                        <a href="#" class="btn btn-primary">Create New Network</a>-->
                                            </p>
                                       </div>
                                       </div>
                                    </div>
                            
                                    
                                    <!-- Card Component Rendering Start -->
                                    <card v-for="card in 7">
                                        
                                     </card>    
                                    <!-- Card Component Rendering End -->
                                    
                                    
                                    
                                    
                                    </div>
                                 </div>
    </div>
    </div>
    <chart></chart>
    <search></search>
    <bar></bar> 
     <GoogleMap></GoogleMap>
    <contact></contact>
    

                        <!-- basic modal -->
    <div class="modal fade"  v-show="show"  id="myModal" tabindex="-1" role="dialog" aria-labelledby="basicModal" aria-hidden="true">
      <div class="modal-dialog">
        <div class="modal-content">
        <div class="modal-header">
              <button type="button" class="close" data-dismiss="modal">&times;</button>
              <h4>Create New Network</h4>
            </div>
            <div class="modal-body">
                 <form role="form">
                <div class="row">
              <div class="col-sm-6">
                  <label for="networkname">Network name<span class="requiredField">*</span></label>
                  <input type="text" v-model="name" class="form-control" id="networkname" placeholder="Enter Network Name">
                </div>
                    <div class="col-sm-6">
                  <label for="nodes">Number of Nodes</label>
                  <input type="text" v-model="nodes" class="form-control" id="nodes" placeholder="Enter Nodes">
                </div>
                  </div>

                  <div class="row">
                 <div class="col-sm-6">
                  <label for="createMapTopology">Network Topology<span class="requiredField">*</span> </label>
                    <select class="form-control" v-model="selectedTopology">
                                                    <option v-for="topology in topologys">{{topology}}</option>
                                                  </select>
                 </div>


                 <div class="col-sm-6">
                <label for="createMapCountryCode">CC (Country Code)<span class="requiredField">*</span></label>
                <select class="form-control" v-model="SelectedCountryCode">
                                                  <option v-for="code in country">{{code}}</option>
                                                 </select>
                </div>
                 </div>


                  <div class="row">
                 <div class="col-sm-6">
                 <label for="createMapIcc">ICC (ITU-T Carrier Code)<span class="requiredField">*</span></label>
                    <select class="form-control" v-model="SelectedcreateMapIcc">
                                                   <option v-for="MapIcc in MapIcc">{{MapIcc}}</option>
                                               </select>
                </div>


                 <div class="col-sm-6">
             <label for="createMapUAPCode">UAPC(Unique Access Point Code)<span class="requiredField">*</span></label>
                <input type="text" v-model="uapc" class="form-control" name="UniqueCode" onfocus="this.placeholder = ''" placeholder="UAPC" id="createMapUAPCode">
                </div>
                 </div>

                     </form>


            </div>
            <div class="modal-footer">
            <button v-on:click="submit('Network is successfully created')" class="btn btn-success btn-block" data-dismiss="modal"><span class="glyphicon glyphicon-book"></span> Create</button>

            </div>
            <div class="modal-footer">
              <button type="submit" class="btn btn-danger btn-block" data-dismiss="modal"><span class="glyphicon glyphicon-backward"></span> Go To Dashboard</button>

            </div>
        </div>
      </div>
    </div>
    <!--                modal end-->                   
     
</div>
</template>
<script>

    

    
    
  import  card from './card.vue'    
  import  dashboard  from './dashboard.vue'
  import  chart  from './chart.vue'
  import  search  from './search.vue'
  import  bar  from './bar.vue'
  import  contact  from './contact.vue'
  import GoogleMap from './GoogleMap.vue'

    export default{
        components:{
           dashboard,
            card,
            chart,
            search,
            bar,
            GoogleMap,
            contact
            
          
        
        },
        data (){
             return {
                 image2:require("./../assets/add.jpeg.png"),
                 dashboard:'Dashboard/Admin1',
                 
//                modal data
                 show:false,
                 name:'',
                 nodes:'10',
                 topologys:['Mess','Hub','Ring','Linear'],
                 selectedTopology:'Mess',
                 country:['INDIA','USA','UK'],
                 SelectedCountryCode:'INDIA',
                 SelectedcreateMapIcc:'DTS',
                 MapIcc:['DTS','VSNL'],
                 uapc:'23',
                
            }
        },
        methods:{
          
            submit:function(value){
                alert(value)
            }
         
        }
    }
  
    
    
</script>                                        
