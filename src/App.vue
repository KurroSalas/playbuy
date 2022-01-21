<template>
  <div id="app">
  <header>
  <div class="superior-header">
  <Logo />
  <BarraBusqueda/>
  </div>
  <Menu />
  </header>
  <main class="container">
    <CaminoMigas/>
    <div class="dos-columnas">
    <ProductoImagen/>
    <ProductoDatos/>
    </div>
    <ProductoDescripcion/>
   </main>
   <Pie/>
   </div>
</template>

<script>
import Logo from "./components/Logo.vue";
import Menu from "./components/Menu.vue";
import BarraBusqueda from "./components/BarraBusqueda.vue";
import CaminoMigas from "./components/CaminoMigas.vue";
import ProductoImagen from "./components/ProductoImagen.vue";
import ProductoDatos from "./components/ProductoDatos.vue";
import ProductoDescripcion from "./components/ProductoDescripcion.vue";
import Pie from "./components/Pie.vue";

export default {
  name: "App",
  components: {
    Logo,
    BarraBusqueda,
    Menu,
    CaminoMigas,
    ProductoImagen,
    ProductoDatos,
    ProductoDescripcion,
    Pie,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@500&family=Titillium+Web:wght@300;400;700&display=swap");

header {
  margin: 0em;
  padding: 0em;
}

body {
  margin-left: 40px;
  padding: 0px;
  box-sizing: border-box;
}

.superior-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

#app {
  font-family: "Titillium Web", sans-serif;
}
.container {
  max-width: 1200px;
  margin: auto;
}

.dos-columnas {
  display: flex;
  margin: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}
</style>
