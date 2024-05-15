<template>
    <div class="child">
      <h3>Nadia Fadila</h3>
      <button @click="sendData">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Nadia Fadila',
    methods: {
      sendData() {
        this.$emit('data-from-child', 'Nadia Fadila');
      }
    }
  }
  </script>
  
  <style scoped>
  .child {
    margin-top: 10px;
    padding: 10px;
    background-color: #f9f9f9;
    border: 1px solid #ddd;
    border-radius: 5px;
  }
  
  .child h3 {
    margin-top: 0;
    color: #333;
  }
  
  .child button {
    background-color: palevioletred;
    color: #fff;
    border: none;
    padding: 5px 10px;
    border-radius: 3px;
    cursor: pointer;
  }
  
  .child button:hover {
    background-color: #0056b3;
  }
  </style>
  