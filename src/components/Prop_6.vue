<template>
    <div class="hello">
     <button @click="callFromParent" >Click me</button>
      
    </div>
  </template>
  
  <script>
  export default {
    name: 'Prop_6',
    props: {},
    methods: {
        callFromParent(){
            this.$parent.myFunction()
        }
    }
  }
  </script>
  
 