<template>
<div>
           <!-- START Header -->
         <header id="header" class="page-topbar">
    <nav class="navbar navbar-inverse navbar-fixed-top ">

        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">

         <a class="navbar-brand" href="#">
      <img v-bind:src="image3" alt="NPT">
    </a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
       <ul class="nav navbar-nav navbar-right">
           <form class="navbar-form navbar-left">
            <div class="form-group">
              <input type="text" v-model="search"  class="form-control" placeholder="Search">
            </div>
            <button type="submit" v-click="submit" class="btn btn-default">Submit</button>
          </form>
      


           <li class="dropdown" @mouseover="notification =true" @mouseleave="notification =false">
               <a href="#" class="dropdown-toggle icon-menu" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false"><span class="glyphicon glyphicon-bell"></span></a>
              <ul class="dropdown-menu notifications" v-if="notification" @click="notification = false">
                <li><a href="#">Action</a></li>
                <li><a href="#">Another action</a></li>
                <li><a href="#">Something else here</a></li>
                <li role="separator" class="divider"></li>
                <li><a href="#">Separated link</a></li>
              </ul>
            </li>


           <li class="dropdown" @mouseover="msg =true" @mouseleave="msg=false">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false"><span class="glyphicon glyphicon-envelope"></span></a>
              <ul class="dropdown-menu" v-if="msg" @click="msg =false">
                <li><a href="#">Action</a></li>
                <li><a href="#">Another action</a></li>
                <li><a href="#">Something else here</a></li>
                <li role="separator" class="divider"></li>
                <li><a href="#">Separated link</a></li>
              </ul>
            </li>

            <li class="dropdown" @mouseover="account =true" @mouseleave="account=false">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false"><span class="glyphicon glyphicon-user"></span></a>
              <ul class="dropdown-menu" v-if="account" @click="account=false">

               <li><a href="#"><i class="glyphicon glyphicon-user"></i> <span>My Profile</span></a></li>
               <li><a href="#"><i class="glyphicon glyphicon-envelope"></i> <span>Message</span></a></li>
               <li><a href="#"><i class="glyphicon glyphicon-cog"></i> <span>Settings</span></a></li>
               <li><a href="#"><i class="glyphicon glyphicon-off"></i> <span>Logout</span></a></li>
              </ul>
            </li>
          </ul>
        </div><!-- /.navbar-collapse -->
     <!-- /.container-fluid -->
    </nav>
       </header>
    <!-- second fixed navbar-->
  </div>

</template>
<script>
  import  navbar  from './navbar.vue'
  
  
    
    export default{
        components:{
            navbar,
           
        },
        data (){
             return {
                 image3:require("./../assets/logo.png"),
                 search:"",
                 notification: false,
                 msg: false,
                 account: false
                
            }
        },
        methods:{
            submit(){
                
            }
        }
       
    }
  
    
    
</script>                                        
