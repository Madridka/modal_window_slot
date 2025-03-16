<template>
  <div>
    <button @click="isModalOpen = true"></button>
    <ModalWindow>

    </ModalWindow>
  </div>
</template>

<script>
import ModalWindow from "./components/ModalWindow.vue";

export default {
  name: "App",
  components: {
    ModalWindow,
  },
  data() {
    return {
      isModalOpen: false,
    };
  },
};
</script>

<style>
</style>
