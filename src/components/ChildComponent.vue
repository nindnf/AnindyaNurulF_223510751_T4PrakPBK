<!-- PinkChildComponent.vue -->
<template>
    <div class="child-component">
      <h3 style="color: #ff0066;">Child Component</h3>
      <button @click="sendDataToParent">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendDataToParent() {
        this.$emit('childData', 'Tugas 4 Praktikum PBk');
      }
    }
  };
  </script>
  
  <style scoped>
  .child-component {
    background-color: #fbf5cf;
    padding: 10px;
    border-radius: 5px;
  }
  
  /* Menentukan warna teks untuk komponen anak */
  .child-component h3 {
    color: rgb(46, 39, 39); /* Warna teks hitam */
  }
  </style>
  