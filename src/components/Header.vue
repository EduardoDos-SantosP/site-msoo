<template>
  <header
      id="Header"
      class="container-fluid h-auto py-2 bg-gradient border-bottom shadow-sm"
  >
    <div class="row h-100 align-items-center">
      <h1 class="text-center fs-2 m-0">Projeto de MSOO</h1>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style scoped>
#Header {
  position: sticky;
  top: 0;
  height: 50px;
  margin-bottom: 80px;
  background-color: var(--bs-gray-800);
  border-color: silver !important;
  z-index: 2;
}
</style>