<template>
<div>
  <p>{{msg}}</p>
  <div class="button-group">
    <button class="button" @click="selectedComp='greeting'">Greeting</button>
    <button class="button" @click="selectedComp='user'">User</button>
  </div>
  <keep-alive>
  <component :is="selectedComp" :age="age"></component>
  </keep-alive>
</div>
</template>

<script>
import greeting from './components/Greeting.vue'
import user from './components/User.vue'
export default{
  name: 'App',
  data(){
    return {
      msg: 'Heloofdfdf',
      age: 40,
      selectedComp:'greeting'
    }
  },
  components:{
    greeting,
    user
  },
  methods:{
    updateChangedAge(){
      this.age++
    }
  }
}


</script>

<style>

</style>
