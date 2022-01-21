<template>
  <section class="menu-principal">
    <nav>
      <Dropdown title="Services" :items="services" />
    </nav>
    <div class="grupo">
      <a class="registro" href="#">REGISTRO</a>
      <a class="login" href="#">INICIAR SESIÓN</a>
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
          title: "Web",
          link: "#",
        },
        {
          title: "Design",
          link: "#",
        },
        {
          title: "Videos",
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
  margin-left: 2.5em;
  font-size: 1.5rem;
}

nav .menu-item {
  padding: 10px 10px 8px;
  margin-left: 0em;
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
  position: relative;
  margin-right: 10em;
  margin-top: 1.25em;
  color: white;
}

.registro {
  margin-right: 1em;
  border: solid;
  padding: 0.5em;
  border-radius: 50px;
  border-color: rgb(27, 112, 221);
  background-color: rgb(27, 112, 221);
}

.login {
  border: solid;
  padding: 0.5em;
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
  display: flex;
  flex-direction: row;
  justify-content: space-between;
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
</style>