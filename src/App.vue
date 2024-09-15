<template>
  <h1>{{ topic }}</h1>
  <p>{{ dang }}</p>

  <div v-if="showModal">
    <CustomModal header="uffs how long" :dang="dang" theme="sale" @close="toggleModal">

      <h1>HOLO</h1>
      <p>SOLO</p>

      <template v-slot:link>
        <a href="#">More Info</a>
        <h3>MAN</h3>
      </template>

    </CustomModal>

  </div>

  <div v-if="showModalTwo">
    <CustomModal header="uffs how long" :dang="dang" @close="toggleModalTwo">

    </CustomModal>

  </div>

  <button @click="toggleModal">Show Modal One</button>
  <button @click="toggleModalTwo">Show Modal Two</button>

</template>

<script>
import CustomModal from './components/CustomModal.vue';

export default {
  name: 'App',
  components: {
    CustomModal
  },
  data() {
    return {
      topic: 'VUE LEARN',
      dang: 'yup',
      showModal: false,
      showModalTwo: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo
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

a {
  color: rgb(107, 209, 238);
  text-decoration: none;
  border: 1px solid #eee;
  border-radius: 4px;
  margin: 10px 0;
  padding: 5px;
}

button{
  margin: 5px;
  color: #2c3e50;
  border-radius: 8px;
  background-color: #dfd;
  font-weight: 800;
  font-size: larger;
}
</style>
