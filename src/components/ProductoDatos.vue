<template>
  <section id="producto-datos">
    <h1>Mini Cooper</h1>
    <h2>59,99€</h2>
    <div class="wrapper">
      <button
        class="btn"
        @click="cambiarContador('-1')"
        type="button"
        name="button"
      >
        <span class="material-icons">remove</span>
      </button>
      <input class="cantidad" type="text" name="name" :value="contador" />
      <button
        class="btn"
        @click="cambiarContador('1')"
        type="button"
        name="button"
      >
        <span class="material-icons">add</span>
      </button>
    </div>
    <br />
    <button class="boton">
      <span class="material-icons">add_shopping_cart</span> AÑADIR CARRITO
    </button>

    <div class="clear">&nbsp;</div>
    <img
      class="fot"
      src="..//assets/war.jpg"
      alt="Portátil Huawei MateBoot X"
    />
    <div class="clear">&nbsp;</div>
  </section>
</template>

<script>
export default {
  Name: "ProductoDatos",
  data() {
    return {
      contador: 1,
    };
  },
  methods: {
    cambiarContador(num) {
      this.contador += +num;
      if (!isNaN(this.contador) && this.contador < 0) {
        this.contador = 0;
      }
    },
  },
};
</script>

<style scoped>
section#producto-datos {
  margin-top: 2em;
  display: flex;
  flex-direction: column;
}
h1 {
  font-size: 2.2rem;
  color: darkblue;
}
h2 {
  font-size: 1.7rem;
  color: rgb(27, 112, 221);
}

.wrapper {
  height: 2rem;
  display: flex;
}

.cantidad {
  border: none;
  text-align: center;
  width: 2rem;
  font-size: 1.2rem;
  border: 1px solid #d8d8d8;
  color: darkblue;
}
.btn {
  display: flex;
  border: 1px solid #d8d8d8;
  width: 1.8rem;
  align-items: center;
  justify-content: center;
}
button:focus,
input:focus {
  outline: 0;
}

.boton {
  background-color: rgb(27, 112, 221);
  font-size: 1.2rem;
  font-weight: 700;
  color: white;
  padding: 0.7rem 1.2rem;
  cursor: pointer;
  border: none;
  border-radius: 50px;
}

.material-icons {
  display: flex;
  justify-content: center;
  align-items: center;
}

.clear {
  display: flex;
  flex-grow: 1;
}
</style>