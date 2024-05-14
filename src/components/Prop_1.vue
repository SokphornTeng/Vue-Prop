<template>
    <div class="hello">
      <h1>{{ myTitle }}</h1>
      <p>{{ showing }}</p>
      <p>{{ myAge }}</p>
   
    </div>
  </template>
  
  <script>
  export default {
    name: 'Prop_1',
    props: {
        myTitle: String,
        showing: String,
        myAge: Number
    }
  }
  </script>
  
 