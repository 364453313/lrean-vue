<template>
  <div>
    <h3>学校：{{school}}</h3>
    <button @click="showName">展示</button>
  </div>
</template>

<script>
export default {
    name:'School',
    data(){
        return {
            school:'社会大学'
        }
    },
    methods: {
        showName(){
            alert(this.school)
        }
    },
}
</script>

<style>

</style>