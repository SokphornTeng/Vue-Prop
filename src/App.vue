<template>
  <div id="app">
    <Prop_1 myTitle="This is Prop" showing="Hi Sokphorn" myAge="26" />
    <hr>
    <Prop_2 firstName="Sokphorn" lastName="Teng" />
    <hr>
    <Prop_3 :myList="myList" />
    <hr>
    <Prop_4 :myName="name" colorBkg="red" />
    <Prop_4 :myName="name" colorBkg="green"/>
    <hr>
    <Prop_5 :user="signUp ? 'Logout' : 'Login'" bgColor="green" />
    <hr>
    <Prop_6 />
    <h3>{{ myMessage }}</h3>
    <hr>
    <Prop_7 :name="listName" />
    <hr>
    <Prop_01  @myClick="handleAction"/>
    <h1>{{ showing }}</h1>
    <hr>
    <Prop_02 v-for="list in foods"
     :key="list.name" 
     :fname="list.name" 
     :fdesc="list.desc" 
     :ffavorite="list.favorite" 
     @take-favorite="getFromChild" />

  </div>
</template>

<script>
import Prop_1 from './components/Prop_1.vue'
import Prop_2 from './components/Prop_2.vue'
import Prop_3 from './components/Prop_3.vue'
import Prop_4 from './components/Prop_4.vue'
import Prop_5 from './components/Prop_5.vue'
import Prop_6 from './components/Prop_6.vue'
import Prop_7 from './components/Prop_7.vue'
import Prop_01 from './components/Prop_01.vue'
import Prop_02 from './components/Prop_02.vue'

export default {
  name: 'App',
  components: {
    Prop_1,
    Prop_2,
    Prop_3,
    Prop_4,
    Prop_5,
    Prop_6,
    Prop_7,
    Prop_01,
    Prop_02
  },
  data(){
    return {
      myList: "Hello Sokphorn this is your practice props",
      name: "SK Teng",
      signUp: true,
      myMessage: '',
      listName: 'SK Teng',
      showing: '',
      foods: [
        { name: 'Apples', desc: 'Apples are a type of fruit that grow on trees.', favorite: true},
        { name: 'Pizza', desc: 'Pizza has a bread base with tomato sauce, cheese, and toppings on top.', favorite: false},
        { name: 'Rice', desc: 'Rice is a type of grain that people like to eat.', favorite: false},
        { name: 'Fish', desc: 'Fish is an animal that lives in water.', favorite: true},
        { name: 'Cake', desc: 'Cake is something sweet that tastes good.', favorite: false}
      ]
    }
  },
  methods: {
    myFunction(){
      this.myMessage = "Hello sis Sokphorn"
    },
    handleAction(data){
      this.showing = data
    },
    getFromChild(){
      alert("Hi child")
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
