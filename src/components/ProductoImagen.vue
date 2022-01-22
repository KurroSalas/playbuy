<template>
  <section id="producto-imagen">
      <div class="img-big"> 
          <img v-bind:src="fotos[0]" alt="Playmobil Mini Cooper" copyright="cc-0">
      </div>
        <div class="img-mini">
          <a @mouseover="cambiarFoto(1)"><img  v-bind:src="fotos[1]" alt="Playmobil Mini Cooper" copyright="cc-0"></a>
          <a @mouseover="cambiarFoto(2)"><img  v-bind:src="fotos[2]" alt="Playmobil Mini Cooper" copyright="cc-0"></a>
          <a @mouseover="cambiarFoto(3)"><img  v-bind:src="fotos[3]" alt="Playmobil Mini Cooper" copyright="cc-0"></a>
          <a @mouseover="cambiarFoto(4)"><img  v-bind:src="fotos[4]" alt="Playmobil Mini Cooper" copyright="cc-0"></a>
        </div>
      </section>    
</template>

<script>
export default {
    Name: 'ProductoImagen',
    data () {
        return {
            fotos: [
                require ('../assets/a1.jpg'),
                require ('../assets/a1.jpg'),
                require ('../assets/a2.png'),
                require ('../assets/a3.png'),
                require ('../assets/a4.jpg')]
        };
    },
    methods: {
        cambiarFoto(id) {
            this.fotos[0] = this.fotos[id];
            this.$forceUpdate();
            
        },
    },

}
</script>

<style scoped>
#producto-imagen {
    border-radius: 1.563rem;
    padding: 1rem;
    margin: 1rem;
    
}
.img-mini {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-top:1em;
    cursor: pointer;
    max-width: 5%;
    height: auto;
}
    
}
.img-mini img {
    width: 9.375rem;
    border:0.125rem solid #d8d8d8;
    
}

.img-big{
    max-width: 5%;
    height: auto;
}
</style>