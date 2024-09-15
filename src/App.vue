<template>
  <h1>{{ topic }}</h1>
  <input type="text" ref="name">
  <button @click="handleClick" >Click</button>

  <CustomModal />
</template>

<script>
import CustomModal from './components/CustomModal.vue';

export default {
  name: 'App',
  components:{
    CustomModal
  },
  data(){
    return{
      topic:'VUE LEARN'
    }
  },
  methods:{
    handleClick(){
      console.log(this.$refs.name)
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()
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
