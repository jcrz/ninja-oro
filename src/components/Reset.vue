<template>
  <div class="container">
    <b-button pill variant="warning" @click="resetear">Reset</b-button>
  </div>
</template>

<script>
import store from "@/store";

export default {
  name: "Reset",
  methods: {
    resetear() {
      if (window.confirm("Está seguro de querer borrar el historial?")) {
        store.resetear();
      }
    }
  }
};
</script>

<style scoped>
.container {
  background-color: rgb(13, 62, 134);
  padding: 12px;
  text-align: center;
}
</style>