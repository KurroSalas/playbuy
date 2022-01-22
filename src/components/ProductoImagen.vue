<template>
  <section id="producto-imagen">
      <div class="img-big"> 
          <img v-bind:src="fotos[0]" alt="Portátil Huawei MateBoot X">
      </div>
        <div class="img-mini">
          <a @mouseover="cambiarFoto(1)"><img  v-bind:src="fotos[1]" alt="Portátil Huawei MateBoot X"></a>
          <a @mouseover="cambiarFoto(2)"><img  v-bind:src="fotos[2]" alt="Portátil Huawei MateBoot X"></a>
          <a @mouseover="cambiarFoto(3)"><img  v-bind:src="fotos[3]" alt="Portátil Huawei MateBoot X"></a>
          <a @mouseover="cambiarFoto(4)"><img  v-bind:src="fotos[4]" alt="Portátil Huawei MateBoot X"></a>
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
    border-radius: 25px;
    padding: 1rem;
    margin: 1rem;
    
}
.img-mini {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-top:1em;
    cursor: pointer;
    
}
.img-mini img {
    width: 150px;
    border:2px solid #d8d8d8;
    
}
</style>