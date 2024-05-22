<template>
    <div class="nested-component">
      <h2>Nested Component</h2>
      <slot></slot>
    </div>
  </template>
  
  <script>
  export default {
  };
  </script>
  
  <style scoped>
  .nested-component {
    background-color: #fff3e0;
    padding: 20px;
    margin: 10px 0;
    border-radius: 8px;
    text-align: center;
  }
  
  h2 {
    color: #ef6c00;
  }
  </style>
  