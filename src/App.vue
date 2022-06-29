<template>
  <div id="app">
    <Header></Header>
    <Index></Index>
    <Footer></Footer>
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.min.css'
import 'bootstrap/dist/js/bootstrap.min'
import Header from "@/components/Header";
import Index from "@/components/Index";
import Footer from "@/components/Footer";
export default {
  name: 'App',
  components: {Footer, Header, Index}
}
</script>

<style>
:root {
  --detail-color: #0cadf2;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  color: var(--detail-color/*--bs-light*/);
}
a {
  text-decoration: none;
}
#app {
  min-height: 100vh;
  background-color: hsl(210, 20%, 20%);
}
.bg-gradient {
  background-image: linear-gradient(-15deg, #00000030, transparent, #fff1) !important;
  background-repeat: no-repeat;
}
</style>
