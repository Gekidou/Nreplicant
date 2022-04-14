<!-- Template -->
<template>
  <div>
    <div class="banner-breed">
      <h1>​Explicando por que existen " razas de perros "</h1>
    </div>

    <b-container>
      <b-row>
        <b-col class="txtIzq p-5">
          Una raza de perro está representada por un número suficiente de individuos que transfieren de manera estable sus características específicas a través de generaciones. Los perros de la misma raza tienen características similares en apariencia y comportamiento, sobre todo porque vienen de un sistema selecto de antepasados que tenían las mismas características.1​ Los perros de una raza específica o raza verdadera, producen animales muy similares a los padres. Un perro se nombra miembro de una raza a través de pruebas de ascendencia, mediante el análisis genético (ADN) o registros escritos de su ascendencia (pedigrí). Sin esas pruebas, la identificación de una raza específica no es confiable.2​ Estos registros, llamado registro de raza, pueden estar en manos de particulares, clubes u otras organizaciones.

Muchas razas tradicionales de perros reconocidas por las principales asociaciones de registros caninos se denominan “razas puras”. Solamente individuos cuyos padres y ancestros son de pura raza se consideran pertenecientes a dicha raza. Este concepto ha causado controversia debido a la dificultad de regulación y debido a las posibles consecuencias genéticas de una población limitada (endogamia). Se han realizado trabajos recientes para clasificar las distintas razas, con algunos resultados que sorprendían con respecto a las estimaciones de edad de la raza y sus interrelaciones con otras castas.

Generalmente, antes de que un tipo de perro se reconozca como de verdadera raza, debe demostrarse que el acoplamiento de un par de ese tipo produce siempre perros que tienen las mismas características que los padres, tanto en aspecto como en comportamiento. Esto se conoce como resultado positivo de raza. Existen muchos interrogantes relacionados con lo que se considera resultado positivo de raza.
        </b-col>
      </b-row>
    </b-container>

    <div class="breed container">
      <v-container>
        <v-row>
          <v-col md="4" v-for="(raza, i) in razas" :key="i">
            <Cardbreed :raza="raza" />
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<!-- Script -->
<script>
import Cardbreed from "@/components/breed/Cardbreed.vue";
import { mapState } from "vuex";
export default {
  name: "Breed",
  computed: {
    ...mapState(["razas"]),
  },
  components: {
    Cardbreed,
  },
};
</script>

<!-- Style -->
<style lang="scss">
.breed {
  margin-bottom: 100px;
}
.banner-breed {

  padding: 20px;
  text-shadow: 0.1em 0.1em #333;
  margin-bottom: 10px;
}
.cardsGroup {
  justify-content: center;
}
.txtIzq {
  background-color: rgb(149, 115, 228);
  color: #ffffff;
  text-align: left;
}
</style>
