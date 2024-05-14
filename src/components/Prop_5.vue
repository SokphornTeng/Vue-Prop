<template>
    <div class="hello">
      <button :style="{background: bgColor}">{{ user }}</button>
   
    </div>
  </template>
  
  <script>
  export default {
    name: 'Prop_5',
    props: {
        user: Boolean,
        bgColor: String
    }
  }
  </script>
  
 