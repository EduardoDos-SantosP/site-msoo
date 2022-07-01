<template>
  <footer
      id="Footer"
      class="container-fluid py-3 border-top shadow-lg"
  >
    <div class="container-fluid">
      <div class="row h-100 justify-content-center">
        <div class="col-footer col-lg-3 col-sm-4 text-start">
          <div class="fw-bold mb-2">Tecnologias utilizadas:</div>
          <div v-for="(technology, i) in technologies" :key="i" class="p-0">
            <a :href="technology.url" target="_blank">{{ technology.name }}</a>
          </div>
        </div>
        <div class="col-footer col-lg-3 col-sm-4 text-center">
          <div class="fw-bold mb-2">Outros Links:</div>
          <div v-for="(otherLink, i) in otherLinks" :key="i" class="p-0">
            <a :href="otherLink.url" target="_blank">{{ otherLink.name }}</a>
          </div>
        </div>
        <div class="col-footer col-lg-3 col-sm-4 text-end">
          <div class="fw-bold mb-2">Membros do grupo:</div>
          <div v-for="(author, i) in authors" :key="i" v-text="author"></div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      authors: ['Eduardo dos Santos Pires', 'Marcos Antônio da Costa Filho', 'Vinicius Oliveira Silva'],
      technologies: [
        { name: 'Bootstrap', url: 'https://getbootstrap.com/docs/5.2/getting-started/introduction/' },
        { name: 'Vue.js', url: 'https://vuejs.org/guide/introduction.html' }
      ],
      otherLinks: [
        { name: 'Simples implementação em PHP', url: 'https://github.com/EduardoDos-SantosP/msoo' }
      ]
    }
  }
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

@media  (max-width: 766px) {
  .col-footer.text-start, .col-footer.text-center { text-align: right !important; margin-top: 20px }
}
</style>