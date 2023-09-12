<template>
  <div class="container">
    <div class="content">
      <h1>My App</h1>
      <p>
        This is an example of how you might use vue Teleport. I think it is a
        pretty neat API that is yet another awesome escape hatch that Vue
        provides for practical reasons.
      </p>
      <button @click="showModal = true">Show Modal</button>
      <teleport to="#modal-root">
        <Modal v-show="showModal" @close="showModal = false">
          This is the Secret modal message!
        </Modal>
      </teleport>
    </div>
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  components: {
    Modal,
  },
  data() {
    return {
      showModal: false,
    };
  },
  methods: {},
};
</script>

<style>
html,
body,
#app {
  margin: 0;
  padding: 0;
  height: 100%;
}

#app {
  font-family: Avenir, Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
  height: 100%;
  display: grid;
  justify-content: center;
  align-items: center;
}

.content {
  max-width: 400px;
  position: relative;
}
</style>
