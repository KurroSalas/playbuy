<template>
  <section class="menu-principal">
    <div class="header-inferior">
    <nav>
      <Dropdown title="Services" :items="services" />
    </nav>
    <div class="grupo">
      <a class="registro" href="#">REGISTRO</a>
      <a class="login" href="#">INICIAR SESIÓN</a>
      <a class="cesta"><svg xmlns="http://www.w3.org/2000/svg" height="48px" viewBox="0 0 24 24" width="48px" fill="#FFFFFF"><path d="M0 0h24v24H0V0z" fill="none"/><path d="M15.55 13c.75 0 1.41-.41 1.75-1.03l3.58-6.49c.37-.66-.11-1.48-.87-1.48H5.21l-.94-2H1v2h2l3.6 7.59-1.35 2.44C4.52 15.37 5.48 17 7 17h12v-2H7l1.1-2h7.45zM6.16 6h12.15l-2.76 5H8.53L6.16 6zM7 18c-1.1 0-1.99.9-1.99 2S5.9 22 7 22s2-.9 2-2-.9-2-2-2zm10 0c-1.1 0-1.99.9-1.99 2s.89 2 1.99 2 2-.9 2-2-.9-2-2-2z"/></svg></a>
    </div>
    </div>
  </section>
</template>

<script>
import Dropdown from "./Dropdown";
export default {
  name: "Menu",
  components: {
    Dropdown,
  },
  data() {
    return {
      services: [
        {
          title: "Vehiculos",
          link: "#",
        },
        {
          title: "Figuras",
          link: "#",
        },
        {
          title: "Especiales",
          link: "#",
        },
      ],
    };
  },
};
</script>

<style>
nav {
  display: flex;
  font-size: 1.5rem;
}

nav .menu-item {
  
  margin-left: 2em;
  font-size:1.2rem;
  position: relative;
  text-align: center;
  justify-content: center;
  display: flex;
  transition: 0.4s;
  cursor: pointer;
  color:darkblue;
  padding-top:1em;
  
  
}

nav .menu-item a {
  color: inherit;
  text-decoration: none;
  
  
}

.grupo {
  display:flex;
  flex-wrap:wrap;
  align-items:center;
  position: relative;
  margin-left: 2em;
  margin-right: 10em;
  color: white;
}

.registro {
  position: relative;
  margin-right: 1em;
  border: solid;
  padding:1em;
  margin-top:0.5em;
  border-radius: 50px;
  border-color: rgb(27, 112, 221);
  background-color: rgb(27, 112, 221);
}

.login {
  position: relative;
  margin-right: 1em;
  border: solid;
  padding: 1em;
  margin-top:0.5em;
  border-radius: 50px;
  border-color: rgb(27, 112, 221);
  background-color: rgb(27, 112, 221);
}

.login:hover,
.registro:hover {
  background-color: rgba(193, 235, 255, 1);
  color: rgb(27, 112, 221);
  font-weight: bolder;
}

.grupo a {
  color: inherit;
  text-decoration: none;
}

.menu-principal {
  background: rgb(27, 112, 221);
  background: rgb(50, 128, 228);
  background: linear-gradient(
    167deg,
    rgba(50, 128, 228, 1) 0%,
    rgba(193, 235, 255, 1) 50%,
    rgba(248, 253, 255, 1) 95%
  );
  border-radius: 18px 0px 0px 18px;
  margin-left: 1em;
  margin-top: 1em;
  padding: 1em;
}

.cesta {
  position: relative;
  background-color: rgb(27, 112, 221);
  padding: 1em;
  margin-top:0.5em;
  cursor: pointer;
  border: none;
  border-radius:50px;
  }

.header-inferior{

  display: flex;
  flex-direction: row;
  justify-content: space-between;
  flex-wrap: wrap;
  max-width: 1200px;
  margin: auto;
}
</style>