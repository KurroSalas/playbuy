<template>
  <section id="camino-migas">
    <BreadCrumb
      class="row justify-content-center mt-4"
      :crumbs="crumbs"
      @selected="selected"
    />
  </section>
</template>

<script>
import BreadCrumb from "./BreadCrumb";
export default {
  name: "CaminoMigas",
  components: { BreadCrumb },
  data() {
    return {
      crumbs: ["Home", "Vehiculos", "Mini Cooper"],
    };
  },
  methods: {
    selected(crumb) {
      console.log(crumb);
    },
  },
};
</script>

<style scoped>
section#camino-migas {
  margin-top: 1em;
  display: flex;
  justify-content: center;
  flex-wrap:wrap;
}
</style>