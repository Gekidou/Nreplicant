<template>
  <div id="app">
    <Navbar />
    <div  class="botonera" id="nav">
      <router-link to="/"><b-button class="btnHome">Presentacion</b-button></router-link> 
      <router-link to="/about"><b-button class="btnMision">explicando</b-button></router-link>     
       <router-link to="/breed"><b-button class="btnRazas">¿que son las razas?</b-button></router-link>  
      <router-link to="/enfermedades"><b-button class="btnTips">Enfermedades Genéticas</b-button></router-link> 
     <router-link to="/adoption"><b-button class="btnAdopta">Adopta NO COMPRES</b-button></router-link>
      <router-link to="/contact"><b-button class="btnContacto">Contacto</b-button></router-link> 
      <router-link to="/admin"><b-button class="btnAdmin">Administrador</b-button></router-link> 
    </div>
    <router-view/>
    <Footer />
  </div>
</template>

<!-- Script -->
<script>
import Navbar from "@/components/appelements/Navbar.vue";
import Footer from "@/components/appelements/Footer.vue";
import { mapActions } from 'vuex';
export default {
  name: "App",
  components: {
    Navbar,
    Footer,
  },
  methods: {
    ...mapActions(["getDataRazas"]),
    ...mapActions(["getDataAdoptados"]),
    ...mapActions(["getDataTips"]),  
  },
   created () {
    this.getDataRazas();
    this.getDataAdoptados();
    this.getDataTips();
  },
};
</script>

<!-- Style -->
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50c2;
}
.botonera {
  background-color: #6c757d;
  color: #ffffff !important;
  padding: 10px;
  display: block;
}
.btnHome {
  color: #ffffff !important;
  background-color: #ffba00 !important;
  margin-left: 3px;
  margin-Right: 3px;
}
.btnMision {
  color: #ffffff !important;
  background-color: #f72585 !important;
  margin-left: 3px;
  margin-Right: 3px;
}
.btnRazas {
  color: #ffffff !important;
  background-color: #7209b7 !important;
  margin-left: 3px;
  margin-Right: 3px;
}
.btnTips {
  color: #ffffff !important;
  background-color: #3a0ca3 !important;
  margin-left: 3px;
  margin-Right: 3px;
}
.btnAdopta {
  color: #ffffff !important;
  background-color: #4361ee !important;
  margin-left: 3px;
  margin-Right: 3px;
}
.btnContacto {
  color: #ffffff !important;
  background-color:  #4cc9f0 !important;
  margin-left: 3px;
  margin-Right: 3px;
}
.btnAdmin {
  color: #ffffff !important;
  background-color: #1DD3B0 !important;
  margin-left: 3px;
  margin-Right: 3px;
}
.btnEditor {
  color: #ffffff !important;
  margin-left: 3px;
  margin-Right: 3px;
}


@media (max-width: 768px) {
  .botonera {
    display: none;
  }
}
</style>