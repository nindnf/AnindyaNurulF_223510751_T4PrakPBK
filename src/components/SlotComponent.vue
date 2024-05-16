<!-- SlotComponent.vue -->
<template>
    <div class="slot-component">
      <h3 style="color: #ff0066;">Slot Component</h3>
      <slot></slot>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        slotData: 'Parent And Child Componen'
      };
    }
  };
  </script>
  
  <style scoped>
  .slot-component {
    background-color: #fbf5cf;
    padding: 10px;
    border-radius: 5px;
  }
  </style>
  