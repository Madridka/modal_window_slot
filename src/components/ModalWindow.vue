<template>
  <div class="modal" v-if="isVisible">
    <div class="modal-content">
      <button @click="closeModal">Close</button>
      <slot>Тут контент</slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "ModalWindow",
  props: {
    isVisible: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    closeModal() {
      this.$emit("close");
    }
  }
};
</script>

<style>
.modal {
  max-width: 400px;
  background: rgba(121, 117, 117, 0.5);
  display: flex;
  align-content: center;
  justify-content: center;
}

</style>