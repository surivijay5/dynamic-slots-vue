<template>
<Form>
    <template v-slot:header>
          <p> User is {{age}} years old</p>{{ageDoubled}}
          <input type="text" />
    </template>
</Form>
</template>

<script>
import Form from './Form.vue'
export default {
    name: 'User',
    components:{
        Form
    },
    props:{
        age:{
            type: Number,
            required:true,
            validator(value){
                return value > 30
            }
        }
    },
    computed:{
        ageDoubled(){
            return this.age * 2
        }
    },
    data(){
        return {
        }
    },

}
</script>

<style>

</style>