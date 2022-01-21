<template>
  <section id="camino-migas">
    <breadcrumb
      class="row justify-content-center mt-4"
      :crumbs="crumbs"
      @selected="selected"
    />
  </section>
</template>

<script>
import breadcrumb from "./breadcrumb";
export default {
  name: "CaminoMigas",
  components: { breadcrumb },
  data() {
    return {
      crumbs: ["Home", "Category", "Sub category"],
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
}
</style>