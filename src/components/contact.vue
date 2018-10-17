<template>
<div>
                       <div class="row">
                    <div class="col-md-12">

                     <div class="panel-heading">
                 <h3 class="panel-title" v-text="paneltitle"></h3>
                
                 </div>   
           <form method="post" action="contact.php" name="contactform" id="contactform">
          <div class="col-md-6">
            <fieldset>
              <input name="name" v-model="name" type="text" id="name" size="30" placeholder="Name">
              <br>
              <input name="email"  v-model="email" type="text" id="email" size="30" placeholder="Email">
              <br>
              <input name="phone" v-model="phone" type="text" id="phone" size="30" placeholder="Phone">
              <br>
              <input name="human" v-model="human" type="text" id="human" size="30" placeholder="Prove your not a robot... What is 2+2?">
              <br>
            </fieldset>
          </div>
          <div class="col-md-6">
            <fieldset>
              <textarea name="comments" v-model="msg" cols="40" rows="20" id="comments" placeholder="Message"></textarea>
            </fieldset>
          </div>
          <div class="col-md-12">
            <fieldset>
              <button type="submit" @click.prevent="submit" class="btn btn-lg" id="submit" value="Submit" style="margin-bottom: 15px;">Send Message</button>
            </fieldset>
          </div>
        </form>
                </div>
          </div>
</div>
</template>
                                        
<script>
  import  contact  from './contact.vue'
  
  
    
    export default{
        components:{
            contact
       
           
        },
        data (){
             return {
              paneltitle:'Contact Us',
                 name:null,
                 email:null,
                 phone:null,
                 human:0,
                 msg:'msg here'
                
            }
        },
        methods:{
            submit(){
                alert('Message was send successfully')
            }
        }
       
    }
  
    
    
</script>       