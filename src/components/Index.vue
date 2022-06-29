<template>
  <main id="Index">
    <div id="content" class="container bg-gradient shadow rounded-3">

      <div
          v-for="(diagram, i) in diagrams"
          :key="i"
          class="card card shadow-sm"
          :class="{ 'mt-5': !!i, 'mb-5': diagrams.length !== i + 1 }"
      >
        <div class="card-header px-3 pt-3">
          <div class="card-title">{{ diagram.label }}</div>
        </div>
        <div class="card-body p-1 px-0">
          <div class="card-img p-0 text-center">
            <img class="diagram-img" :src="getImgUrl(diagram)" :alt="diagram.label">
          </div>
        </div>
      </div>

    </div>
  </main>
</template>

<script>
export default {
  name: "Index",
  data() {
    return {
      diagrams: [
        { label: 'Diagrama de classes', img: 'classes.png' },
        { label: 'Diagrama de casos de uso', img: 'use-cases.png' }
      ]
    }
  },
  methods: {
    getImgUrl(diagram) {
      return window.location.origin + '/imgs/' + diagram.img
    }
  }
}
</script>

<style scoped>
:root {
  --bs-teal-rgb: rgb(32, 201, 151);
  --bs-cyan-rgb: rgb(13, 202, 240);
}
.card {
  background-color: transparent;
}
.card, .card * {
  border-color: silver !important;
}
#content {
  width: 100%;
  max-width: 800px;
  padding: 20px 30px;
  background-color: var(--bs-gray-800);
}
.diagram-img {
  max-width: calc(100vw - 108px);
}
</style>