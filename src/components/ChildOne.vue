<template>
    <div class="child-one">
      <h2>Child One</h2>
      <button @click="sendData">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendData() {
        this.$emit('sendData', 'Data from Child One');
      }
    }
  };
  </script>
  
  <style scoped>
  .child-one {
    background-color: #e3f2fd;
    padding: 20px;
    margin: 10px 0;
    border-radius: 8px;
    text-align: center;
  }
  
  h2 {
    color: #0d47a1;
  }
  
  button {
    padding: 10px 20px;
    background-color: #1976d2;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
  }
  
  button:hover {
    background-color: #1565c0;
  }
  </style>
  