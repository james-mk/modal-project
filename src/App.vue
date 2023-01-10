<template>
  <h1>{{ title }}</h1>
  <p>Welcome.............</p>
  <div v-if="showModal">
    <Modal @closeModal="toggleModal" :theme="theme">
      <h1>Njaanuary Giveaway!!</h1>
      <p>Step up your shoe-game at half the price</p>

      <template v-slot:links>
        <a href="#">Sign Up Now</a>
        <a href="#">Learn More..</a>
      </template>
    </Modal>
  </div>
  <br />
  <button @click="toggleModal">Show Modal</button>
</template>

<script>
import Modal from "./components/Modal.vue";
export default {
  name: "App",

  data() {
    return {
      title: "Vuejs App",
      header: "Njaanuary sale!!!",
      text: "Step up your shoe-game on at half price",
      theme: "sale",
      showModal: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
  },

  components: { Modal },
};
</script>

<style >
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
