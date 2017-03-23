<template> 
    <div class="test">
        <input type="text" v-model="title" >
        <h1>{{title}}</h1>
        <p>{{user.first_name}}</p>
        <button v-on:click = "hello('pulkit')"> say greeting</button>

    </div>

</template>


<script>
   export default {
     name:'test',
     data(){
         return{



             title:'hello world ',
        user:{
            first_name:'pulkit',
            last_name:'bansal'
            }
         }

        

     },

     methods:{
        hello: function(who){
            alert("hello" + who);
        }

     }

   }

</script>




<style scoped>

</style>