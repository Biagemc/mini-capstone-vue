<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <div class="row">
      <div class="col-xl-4" v-bind:key="product.id" v-for="product in products">
        <b-card
          v-bind:title="product.name"
          img-src="product.images.url"
          img-alt="product-image"
          img-top
          tag="article"
          style="max-width: 20rem;"
          class="card mb-2 col-xl-3 "
        >
          <b-card-text>
            {{ product.description }}
          </b-card-text>
          <p>Price: {{ product.price }}</p>
          <b-button href="#" variant="primary">Show Info</b-button>
        </b-card>
      </div>
    </div>
  </div>
</template>

<style></style>

<script>
import axios from "axios";
export default {
  data: function() {
    return {
      message: "Welcome to Mini Capstone Products",
      products: [],
    };
  },
  created: function() {
    axios
      .get("/api/products")
      .then(response => {
        console.log(response.data);
        this.products = response.data;
      })
      .catch(error => {
        this.errors = error.response.data.errors;
      });
  },
  methods: {},
};
</script>
