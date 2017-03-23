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
       <span :class="{contacted: user.contacted}">
       {{user.name}} : {{user.email}}<button v-on:click="deleteUser(user)">x</button>
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
       },

       deleteUser: function(user){

           this.users.splice(this.users.indexOf(user),1);
       }

     }

   }

</script>




<style scoped>

.contacted{

    text-decoration:line-through;
}

</style>