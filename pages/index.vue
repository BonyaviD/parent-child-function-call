<script setup>
import ModalComponent from "~/components/ModalComponent.vue";
import childComponent from "~/components/childComponent.vue";
import { ref } from "vue";

const modal = ref(null);
const child = ref(null);
const toggleModalParent = () => {
  modal.value?.toggleModalCgild();
};
const toggleParent = () => {
  child.value?.toggleComponentChild();
};
</script>

<template>
  <div>
    <ModalComponent ref="modal" />
    <div @click="toggleModalParent" class="btn">Click to open/close ModalChild in ParentComponent</div>
    <childComponent ref="child" />
    <div @click="toggleParent" class="btn">Click to open/close Component in ParentComponent</div>
  </div>
</template>

<style scoped>
.btn {
  width: 100%;
  height: 2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 1rem;
  background-color: rgb(22, 185, 95);
}
</style>
