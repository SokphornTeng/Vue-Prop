<template>
    <div class="hello">
     <button :style="{background: colorBkg}"><h3> {{ myName }}</h3></button> 
   
    </div>
  </template>
  
  <script>
  export default {
    name: 'Prop_4',
    props: {
        colorBkg: String,
        myName: String
    }
  }
  </script>
  
 