<template>
  <div class="container" id="app">
    <ContadorOro :cantidadOros="cantidadOros" />
    <div class="casillas">
      <b-row>
        <b-col cols="3">
          <Casilla titulo="Granja" v-bind:arreglo="[10,20]"/>
        </b-col>
        <b-col cols="3">
          <Casilla titulo="Cueva" v-bind:arreglo="[5,10]"/>
        </b-col>
        <b-col cols="3">
          <Casilla titulo="Casa" v-bind:arreglo="[2,5]"/>
        </b-col>
        <b-col cols="3">
          <Casilla titulo="Casino" v-bind:arreglo="[0,50]"/>
        </b-col>
      </b-row>
    </div>
    <Actividad :actividades="actividades" />
  </div>
</template>

<script>
import ContadorOro from "./components/ContadorOro";
import Casilla from "./components/Casilla";
import Actividad from "./components/Actividad";
import store from '@/store'

export default {
  name: "App",
  components: {
    ContadorOro,
    Casilla,
    Actividad
  },
  data: function(){
    return store.state;
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
  border: 1px solid black;
  padding: 0px;
}
.casillas {
  padding: 0px 30px;
  background-color: rgb(13, 62, 134);
}
</style>
