<template>
<h3>{{ title }}</h3>
<p>Welcome.............</p>
<div v-if="showModal">
  <Modal :header="header" :text="text" :theme="theme" @closeModal="toggleModal"/>
</div>
<br>
<button @click="toggleModal">
Show Modal

</button>

</template>

<script>
import Modal from './components/Modal.vue'
export default {
  name: 'App',

data(){
  return {
    title:'Vue CLI',
    header:'Njaanuary sale!!!',
    text:'Step up your shoe-game on at half price',
    theme:'sale',
    showModal:false
  }
},
methods:{
  toggleModal(){
    this.showModal = !this.showModal
  }

},

components:{Modal}
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
