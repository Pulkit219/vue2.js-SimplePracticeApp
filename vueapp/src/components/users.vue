<template> 
    <div class="users">

    <form v-on:submit="addUser">
    
       <input type="text" v-model="newUser.name" placeholder="enter a name">
       <br/>
       <input type="text" v-model="newUser.emailname" placeholder="enter an email">
       <br/>
       <input type="submit" value="submit">

    </form>

       <ul>

       <li v-for="user in users">{{user.name}} : {{user.email}}</li>
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
           console.log("add");
           e.preventDefault();
       }

     }

   }

</script>




<stytle scoped>

</style>