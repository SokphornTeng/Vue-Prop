<template>
    <div class="hello">
     <h4 >{{ name }}</h4>
      
    </div>
  </template>
  
  <script>
  export default {
    name: 'Prop_7',
    props: {
        name: {
            type: String,
            required: true,
            default: 'Sokphorn SK'
        }
    },
    
  }
  </script>
  
 