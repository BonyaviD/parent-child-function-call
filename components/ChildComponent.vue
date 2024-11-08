<script setup>
// import { defineExpose } from "vue";
import { ref } from "vue";

const ChildComponent = ref(null);

const toggleComponentChild = () => {
  ChildComponent.value = !ChildComponent.value;
};

defineExpose({
    toggleComponentChild,
});
</script>

<template>
  <div class="component-style" v-if="ChildComponent">
    <div>this is a child component</div>
    <div @click="toggleComponentChild">Click to Close Component in ChildComponent</div>
  </div>
</template>

<style>
.component-style {
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
