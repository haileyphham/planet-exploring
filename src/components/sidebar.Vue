<template>
    <div id="sidebar" :class="{ show: isVisible }">
      <h2 id="sidebar-header"></h2>
      <p id="sidebar-content"></p>
      <button id="exit-btn" @click="closeSidebar">
        <h3 id="exit-text">Exit</h3>
      </button>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const isVisible = ref(false);
  
  const closeSidebar = () => {
    isVisible.value = false; // Add your logic to show/hide the sidebar
  };
  
  // Function to show the sidebar
  const showSidebar = () => {
    isVisible.value = true;
  };
  
  // Use the showSidebar function to trigger visibility from other components
  </script>
  
  <style scoped>
  /* Your existing sidebar styles */
  </style>
  