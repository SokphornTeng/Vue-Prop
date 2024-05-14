<template>
    <div class="hello">
      <h3>{{ firstName }} - and - {{ lastName }}</h3>
   
    </div>
  </template>
  
  <script>
  export default {
    name: 'Prop_2',
    props:['firstName', 'lastName']
  }
  </script>
  
 