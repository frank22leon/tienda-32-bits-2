  
<template>
  <div>
    <h1>Ventas</h1>

    <section>
      <h3>Cantidad de Juegos con stock</h3>
      <VentaJuegos :juegos="$store.state.juegos" />
    </section>
    
  </div>
</template>

<script>
import VentaJuegos from "../components/VentaJuegos.vue";
export default {
  name: "Ventas",
  components: {
    VentaJuegos
  },
  methods: {
    vender(producto) {
      this.$store.dispatch("vender", producto);
    },
  },
};
</script>

<style></style>