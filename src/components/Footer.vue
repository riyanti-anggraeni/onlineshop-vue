<script setup>
const tahun = new Date().getFullYear(); 
</script>

<template>
  <footer class="bg-gray-800 text-white py-4">
    <div class="container mx-auto text-center">
      <p>&copy; {{ tahun }} Online Shop. All rights reserved.</p>
    </div>
  </footer>
  </template>

  <style scoped>
.site-footer {
  background-color: #c3cee4;
  color: #82e8f9;
  padding: 20px 16px 28px;
  text-align: center;
  border-top: 1px solid #e5e5e5;
}
</style>