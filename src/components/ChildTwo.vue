<template>
    <div class="child-two">
      <h2>Child Two</h2>
      <button @click="sendData">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendData() {
        this.$emit('sendData', 'Data from Child Two');
      }
    }
  };
  </script>
  
  <style scoped>
  .child-two {
    background-color: #fce4ec;
    padding: 20px;
    margin: 10px 0;
    border-radius: 8px;
    text-align: center;
  }
  
  h2 {
    color: #880e4f;
  }
  
  button {
    padding: 10px 20px;
    background-color: #d81b60;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
  }
  
  button:hover {
    background-color: #c2185b;
  }
  </style>
  