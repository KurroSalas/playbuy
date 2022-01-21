<template>
  <section id="camino-migas">
      <a class="inicio" href="#"> Inicio </a> >
      <a href="#">Ordenadores </a> > 
      <a class="actual" href="#">Ordenador portátil</a> 


  </section>
</template>

<script>
export default {

}
</script>

<style scoped>
section#camino-migas {
    margin-right:10em;
    margin-top:1em;
    display:flex;
    justify-content: center;

}
section#camino-migas a, 
section#camino-migas a:hover, 
section#camino-migas a:visited{
    text-decoration: none;
    font-size: 1.2rem;
    margin-left: 1rem;
    margin-right: 1rem;
    color: rgb(27, 112, 221);
}
section#camino-migas a.actual {
    font-weight: 700;
}

</style>