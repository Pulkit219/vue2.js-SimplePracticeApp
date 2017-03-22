<template> 
    <div class="test">
        <h1>{{title}}</h1>
        <p>{{user.first_name}}</p>

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

        

     }

   }

</script>




<stytle scoped>

</style>