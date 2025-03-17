<template>
  <div>
    <button @click="isModalOpen = true">Открыть модальное окно</button>
    <ModalWindow :is-visible="isModalOpen" @close="isModalOpen = false">
      <h1>Контент модального окна</h1>
      <h3>Если в родительском компоненте тут ничего не будет, то отразиться контент 
        в дочернем компоненте в slot, а именно "Тут контент"</h3>
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
