<template> 
    <div class="users">

    <form v-on:submit="addUser">
    
       <input type="text" v-model="newUser.name" placeholder="enter a name">
       <br/>
       <input type="text" v-model="newUser.email" placeholder="enter an email">
       <br/>
       <input type="submit" value="submit">

    </form>

       <ul>

       <li v-for="user in users">
       <input type="checkbox" class="toggle" v-model="user.contacted">
       <span :class="{contacted: user.conatacted}">
       {{user.name}} : {{user.email}}
        </span>
       
       </li>
       </ul>
    </div>

</template>


<script>
   export default {
     name:'users',
     data(){
         return{

             newUser:{},
           users:[
               {
                   name:'John Doe',
               email:'exmple@gmail.com',
               contacted:false

               },

                {
                   name:'Pulkit Bansal',
               email:'exmple@gmail.com',
               contacted:false

               },


                {
                   name:'John smith',
               email:'exmple@gmail.com',
               contacted:false

               }

           ]


          
         }

        

     },

     methods:{
       addUser: function(e){
         this.users.push(
             {
                 name:this.newUser.name,
                 email:this.newUser.email,
                 conatacted:false
             }
         );
           e.preventDefault();
       }

     }

   }

</script>




<stytle scoped>

</style>