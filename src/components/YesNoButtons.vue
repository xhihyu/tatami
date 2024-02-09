<template>
    <div>
      <button @click="handleYesClick">Yes</button>
      <button @click="handleNoClick">No</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      handleYesClick() {
     
      },
      handleNoClick() {
       
      }
    }
  };
  </script>
  
  <style scoped>
  /* Optional scoped styles for the component */
  button {
    margin: 5px;
    padding: 10px 20px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font: dancing;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  </style>
  