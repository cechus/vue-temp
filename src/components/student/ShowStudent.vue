<template>
  <div>
    <div v-if="! editable">
      Nombre: {{ name }}
      <br>
      Apellido: {{ lastName }}
      <br>
    </div>
    <div v-else>
      <label for>Nombre</label>
      <input type="text" v-model="name">
      <br>
      <label for>Apellido</label>
      <input type="text" v-model="lastName">
    </div>

    <button @click="edit()" class="button " v-bind:class="{'tomato': editable, 'blue-sky': !editable}">editar</button>
  </div>
</template>
<script>
export default {
  mounted() {
    console.log("component mounted");
  },
  data() {
    return {
      editable: false,
      name: "Oscar",
      lastName: "Choque"
    };
  },
  methods: {
    edit() {
      this.editable = ! this.editable;
    }
  }
};
</script>
 <style scoped>
.button {
  border-radius: 8px;
  border: none;
  padding: 5px 10px;
  margin: 10px;
}
.tomato {
  background: tomato;
}
.blue-sky {
  background: skyblue;
}
</style>
 
