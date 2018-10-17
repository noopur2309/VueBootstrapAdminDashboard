<template>
<div>
<div class="row">
<div class="col-md-12">
<!-- RECENT PURCHASES -->
<div class="panel">
<div class="panel-heading">
<h3 class="panel-title" v-text="panelTitle"></h3>
</div>
<div class="panel-body no-padding">

<input class="form-control" id="myInput" type="text" placeholder="Search..">
<br>                                  
<table class="table table-striped">
<thead>
<tr>
<th>Name</th>
<th>State</th>
<th>Cost</th>
<th>Date</th>
<th>Topology</th>
<th>Status</th>
<th>Actions</th>
</tr>
</thead>

<tbody>
<tr v-for="item in items">
<td>{{item.name}}</td>
<td>{{item.state}}</td>
<td>{{item.cost}}</td>
<td>{{item.Date}}</td>
<td>{{item.topology}}</td>
<td><span class="label label-success">COMPLETED</span></td>
<td><a v-on:click="handleClick('test')" href="#" class="OpenMap" title="OpenMap" data-toggle="tooltip"><i class="glyphicon glyphicon-eye-open"> </i></a>
            <a v-on:click="handleClick('second')" href="#" class="Clone" title="Clone" data-toggle="tooltip"><i class="glyphicon glyphicon-pencil"> </i></a>
            <a v-on:click="handleClick('delete')" href="#" class="Delete" title="Delete" data-toggle="tooltip"><i class="glyphicon glyphicon-trash"> </i></a>
                            </td>




</tr>
</tbody>
</table>
</div>
</div>
</div>

</div>




</div>
</template>

<script>
import  search  from './search.vue'



export default{
components:{
search


},
 data (){
             return {
                 panelTitle:'Recent Networks',
            items:[
                {name:'Sample', state:'GreenField' ,topology:'Mess',cost:'$500', Date:'Oct 11,2018'},
                {name:'Network', state:'GreenField' ,topology:'Mess',cost:'$500', Date:'Oct 11,2018'},
                {name:'Sample', state:'GreenField' ,topology:'Mess',cost:'$500', Date:'Oct 11,2018'},
                {name:'Network', state:'GreenField' ,topology:'Mess',cost:'$500', Date:'Oct 11,2018'}
            ],
          
        }

},
     methods:{
            handleClick: function(value)
            {
             alert(value)
            }
           
         
        }

}

</script>                                        
