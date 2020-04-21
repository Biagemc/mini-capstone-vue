<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <div>
      <div class="mt-2">Name: {{ name }}</div>
      <b-form-input v-model="name"></b-form-input>
    </div>
    <div>
      <div class="mt-2">Description: {{ description }}</div>
      <b-form-input v-model="Description"></b-form-input>
    </div>
    <div>
      <div class="mt-2">Price: {{ price }}</div>
      <b-form-input v-model="price"></b-form-input>
    </div>
    <div>
      <div class="mt-2">Supplier Id: {{ supplierId }}</div>
      <b-form-input v-model="supplierId"></b-form-input>
    </div>
  </div>
</template>

<style></style>

<script>
import axios from "axios";
export default {
  data: function() {
    return {
      message: "Products New!",
      name: "",
      description: "",
      price: "",
      supplierId: "",
    };
  },
  created: function() {},
  methods: {},
};
</script>
