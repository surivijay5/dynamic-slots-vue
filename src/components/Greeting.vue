<template>
<Form>
  <p>{{msg}}</p>
  <template v-slot:footer>{{age}} is just a number
    <input type="text" />
  </template>
  
</Form>
</template>

<script>
import Form from './Form.vue'
export default{
  name: 'Greeting',
  props:['age'],
  components:{
    Form
  },
  data(){
    return {
      msg: 'Heloofdfdfdfsdsad'
    }
  },
  methods:{
    updateAge(){
      this.$emit('age-change')
    }
  }
}


</script>

<style>

</style>
