<template>
    <div class="parent">
      <h2>Parent</h2>
      <p>Data from Child: {{ childData }}</p>
      <ChildOne @data-from-child="handleDataFromChild" />
      <ChildTwo @data-from-child="handleDataFromChild" />
    </div>
  </template>
  
  <script>
  import ChildOne from './childone.vue';
  import ChildTwo from './childtwo.vue';
  
  export default {
    name: 'Parent',
    components: {
      ChildOne,
      ChildTwo
    },
    data() {
      return {
        childData: ''
      };
    },
    methods: {
      handleDataFromChild(data) {
        this.childData = data;
      }
    }
  }
  </script>
  
  <style scoped>
  .parent {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    padding: 20px;
    border: 2px solid #ccc;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .parent h2 {
    color: #333;
  }
  
  .parent p {
    color: #666;
  }
  
  /* Stil Child Components */
  .child {
    margin-top: 10px;
    padding: 10px;
    background-color: #fff;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  .child h3 {
    margin-top: 0;
    color: #555;
  }
  </style>