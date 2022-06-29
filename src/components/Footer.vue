<template>
  <footer
      id="Footer"
      class="container-fluid py-3 border-top shadow-lg"
  >
    <div class="container">
      <div class="row h-100 justify-content-center align-items-center">
        <div class="col-lg-4">

        </div>
        <div class="col-lg-4">

        </div>
        <div class="col-lg-4 text-end">
          <div class="fw-bold mb-1">Membros do grupo:</div>
          <div>Eduardo dos Santos Pires</div>
          <div>Marcos Antônio da Costa Filho</div>
          <div>Vinicius Oliveira Silva</div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style scoped>
#Footer {
  min-height: 50px;
  margin-top: 80px;
  background-color: var(--bs-gray-900);
  border-color: silver !important;
  z-index: 2;
}
* {
  color: silver;
}
</style>