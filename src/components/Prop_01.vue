<template>
    <div class="hello">
      <h3>Child emit only event or function to parent</h3>
       <button @click="sendDataToParent">Click me !</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Prop_01',
    methods: {
      sendDataToParent(){
        this.$emit('myClick', 'already clicked!!!')
      }
    }
  }
  </script>
  
 