<template>
  <div :v-if="isVisible = true">
    <div :is-visible="isModalOpen">
      <slot>Default content</slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "ModalWindow",
  props: {
    isModalOpen: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style>
</style>