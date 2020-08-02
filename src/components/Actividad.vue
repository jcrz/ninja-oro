<template>
  <div class="container">
    <b-row>
      <b-col text="left align" cols="12">
        <h6>Historial</h6>
      </b-col>
      <b-col cols="12">
        <b-form-textarea
          id="textarea"
          v-model="actividades"
          placeholder="Esperando actividad..."
          rows="6"
        ></b-form-textarea>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: "Actividad",
  props: {
      actividades: String
  }
};
</script>

<style scoped>
h6 {
  color: white;
}
.container {
  background-color: rgb(13, 62, 134);
  padding: 30px;
}
</style>