<script setup>
// import { defineExpose } from "vue";
import { ref } from "vue";

const modalRef = ref(null);

const toggleModalCgild = () => {
  modalRef.value = !modalRef.value;
};

defineExpose({
    toggleModalCgild,
});
</script>

<template>
  <div class="modal-style" v-if="modalRef">
    <div>this is a Modal</div>
    <div @click="toggleModalCgild">Click to Close Component</div>
  </div>
</template>

<style scoped>
.modal-style {
  width: 100%;
  height: 5rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  background-color: rgb(13, 110, 81);
  margin-top: 1rem;
}
</style>
