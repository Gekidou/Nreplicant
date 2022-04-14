<template>
  <div class="barraNav">
    <b-navbar toggleable type="dark" variant="dark">
      <b-navbar-brand to="/"
        ><li class="patita">N Replicant<i class="fas fa-paw"></i></li
      ></b-navbar-brand>

      <b-navbar-toggle target="navbar-toggle-collapse">
        <template #default="{ expanded }">
          <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
          <b-icon v-else icon="chevron-bar-down"></b-icon>
        </template>
      </b-navbar-toggle>

      <b-collapse id="navbar-toggle-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item to="/">Presentacion</b-nav-item>
          <b-nav-item to="/about">explicando</b-nav-item>
          <b-nav-item to="/breed">¿que son las razas?</b-nav-item>
          <b-nav-item to="/enfermedades">Enfermedades Genéticas</b-nav-item>
          <b-nav-item to="/adoption">Adopta NO COMPRES</b-nav-item>
          <b-nav-item to="/contact">Contacto</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style lang="scss">
.patita {
  list-style: none !important;
  color: #ffffff !important;
}
</style>
