<template>
  <div class="menu-item" @click="isOpen = !isOpen">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      height="48px"
      viewBox="0 0 24 24"
      width="48px"
      fill="#FFFFFF"
    >
      <path d="M0 0h24v24H0V0z" fill="none" />
      <path
        d="M4 18h16c.55 0 1-.45 1-1s-.45-1-1-1H4c-.55 0-1 .45-1 1s.45 1 1 1zm0-5h16c.55 0 1-.45 1-1s-.45-1-1-1H4c-.55 0-1 .45-1 1s.45 1 1 1zM3 7c0 .55.45 1 1 1h16c.55 0 1-.45 1-1s-.45-1-1-1H4c-.55 0-1 .45-1 1z"
      />
    </svg>

    <transition name="fade"> </transition>

    <div class="sub-menu" v-if="isOpen">
      <a href="#" class="material-icons"> home </a>
      <span id="titulo-menu">NUESTRO CATALOGO</span>
      <div v-for="(item, i) in items" :key="i" class="item-menu">
        <a :href="item.link">{{ item.title }}</a>
      </div>
      <span id="acerca">ACERCA DE</span>
      <a class="acerca-menu" href="#">Nosotros</a>
      <a class="acerca-menu" href="#">Condiciones de compra</a>
      <a class="acerca-menu" href="#">Envios y devoluciones</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "dropdown",
  props: ["title", "items"],
  data() {
    return {
      isOpen: false,
    };
  },
};
</script>

<style>
nav .sub-menu {
  display: flex;
  flex-direction: column;
  position: absolute;
  background-color: rgba(193, 235, 255, 1);
  top: calc(100% + 18px);
  left: 50%;
  width: 10em;
  margin-left: -1.5em;
  transform: translate (-50%);
  padding: 3em 1em 1em 1em;

  border-radius: 16px 16px 16px 16px;
  opacity:0.9;
  

}

nav .item-menu{

  margin-top:1em;
}

nav .item-menu:hover {
  background-color: rgba(248, 253, 255, 1);
  border-radius: 16px 16px 16px 16px;
  opacity: 50%;
  color: rgb(27, 112, 221);
  font-weight: bolder;
}

#titulo-menu {
  margin-top: 1em;
  text-decoration-line: underline;
  
  }

#acerca {
  margin-top: 4em;
  text-decoration-line: underline;
}
.acerca-menu {
  padding: 0.5em;
}

nav .acerca-menu:hover {
  background-color: rgba(248, 253, 255, 1);
  border-radius: 16px 16px 16px 16px;
  opacity: 50%;
  color: rgb(27, 112, 221);
  font-weight: bolder;
}

.fade-enter-active,
.fade-leave-active {
  transition: all 0.5s ease-out;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
