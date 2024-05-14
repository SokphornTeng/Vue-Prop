<template>
    <div class="hello">
      <h3>{{ fname }}</h3>
      <p v-show="favoriteActive">My Favorite</p>
      <h4>{{ fdesc }}</h4>
      <button @click="toggleFavorite" >Favorite</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Prop_02',
    props: ['fname', 'fdesc', 'ffavorite'],
    data(){
        return {
            favoriteActive: this.ffavorite
        }
    },
    methods: {
      toggleFavorite(){
        this.$emit('take-favorite')
      }
    }
  }
  </script>
  
 