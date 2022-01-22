<template>
  <section id="barra-busqueda">
      <form @submit.prevent="handleEnviar">
          <input type="text" placeholder="Buscar productos ...">
          <button id="boton-busqueda"><svg id="iconbus" xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000"><path d="M0 0h24v24H0V0z" fill="none"/><path d="M15.5 14h-.79l-.28-.27c1.2-1.4 1.82-3.31 1.48-5.34-.47-2.78-2.79-5-5.59-5.34-4.23-.52-7.79 3.04-7.27 7.27.34 2.8 2.56 5.12 5.34 5.59 2.03.34 3.94-.28 5.34-1.48l.27.28v.79l4.25 4.25c.41.41 1.08.41 1.49 0 .41-.41.41-1.08 0-1.49L15.5 14zm-6 0C7.01 14 5 11.99 5 9.5S7.01 5 9.5 5 14 7.01 14 9.5 11.99 14 9.5 14z"/></svg></button>
      </form>
  </section>
</template>

<script>
export default {
    name: 'BarraBusqueda',
    methods: {
        handleSutmit() {
            console.log("Busqueda enviada")
        }
    }
}
</script>

<style scoped>
section#barra-busqueda {
    margin-right: 5em;
    margin-top:3em;
    
}
section#barra-busqueda form {
    display: flex;
    justify-content: center;
    align-items: center;
}
section#barra-busqueda input{
    margin: 1rem;
    padding: 0.7rem 1rem;
    border-style: solid;
    border: 2px solid rgb(27, 112, 221);
    color: #181818;
    outline: none;
    line-height: 1.4rem;
    border-radius: 50px;
    font-size: 1.2rem;
}
#boton-busqueda {
  background-color: gba(193, 235, 255, 1);
  padding: 1em;
  cursor: pointer;
  border: none;
  border-radius:50px;
  
}

#iconbus{

    margin:0;
    padding-top: 0em;
}

</style>