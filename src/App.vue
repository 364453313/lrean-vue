<template>
    <div>
        <h1>{{msg}}</h1>
        <Student/>
        <School/>
    </div>
</template>

<script>
import School from './components/School.vue'
import Student from './components/Student.vue'

export default {
    name:'App',
    data(){
        return{
            msg:'牛逼的人'
        }
    },
    components:{
        School,
        Student
    }
};
</script>

<style>
</style>