<template>
    <p></p>
    <div class="container">
      <h1 class="alert alert-secondary" role="alert">Ini adalah percobaan</h1>
     <!-- <h2>Name: {{ name }}</h2>
      <button v-on:click="changeName">Change Name</button> -->
      <!-- <input type="text" v-model="search" placeholder="Search..." /> -->

      <div class="hstack gap-3">
      <h2 class="bg-light border">Name: {{ name }}</h2>
      <input class="bg-light border ms-auto" type="text" v-model="name" /> 
      <div class="vr"></div>
        <button class="bg-light border" v-on:click="changeName">Change Name</button>
    </div>
    
    <p></p>
    <p>Makanan </p>
    <input type="text" v-model="search" placeholder="Search..." />
  
    <ul>
      <!-- loop data dari Computed Properties filterProducts -->
      <li v-for="product in filterProducts" v-bind:key="product.id">
        {{ product.title }} - {{ product.price }}
      </li>
    </ul>
    
</div>
  </template>
  
  <script>
  export default {
    name: "App",
    data() {
      return {
        name: "",
        search: "",
        products: [],
      };
    },
    created() {
      this.products = [
        { title: "bakwan" },
        { title: "ketupat" },
        { title: "lontong" },
        { title: "kecap" }
      ];
    },
    // Computed Properties
    computed: {
      filterProducts() {
        // filter product dari array
        return this.products.filter((product) => {
          // Return title = search
          return product.title.match(this.search);
        });
      },
    },
    methods: {
      changeName() {
        this.name = "Muhammad Dicky Farhan";
      },
    },
  };
  </script>