<template>
  <div class="container">
    <b-row>
      <b-col class="casilla">
        <h3>{{ titulo }}</h3>
        <p>{{ arreglo }}</p>
        <b-button @click="numeroAzar" pill variant="info">Buscar Oro</b-button>
      </b-col>
    </b-row>
  </div>
</template>

<script>
import store from "@/store";

export default {
  name: "Casilla",
  props: {
    titulo: String,
    arreglo: Array
  },
  methods: {
    numeroAzar() {
      store.actualizarOros(this.titulo, this.arreglo);
    }
  }
};
</script>

<style scoped>
.casilla {
  padding: 10px;
  border-radius: 13px;
  background-color: darkgoldenrod;
  text-align: center;
}
h3{
  color: white;
}
</style>