<!-- Template -->
<template>
  <div>
    <div class="banner-adoption">
      <h1> ADOPTA NO COMPRES !</h1>
    </div>

    <b-container class="introAdoption p-5">
     Recuerda que un compañero es para siempre...
     ADOPTA Y no promuebas la COMPRA de mascotas El decidir tener un perro o un gato en casa implica mucho más que darle amor y un hogar donde vivir, este acto conlleva importantes responsabilidades para resguardar el bienestar de los animales; obligaciones normadas en la Ley de Tenencia Responsable, que además de proteger a las mascotas, contribuyen a la salud y seguridad pública.
    </b-container>

    <div class="breed container">
      <v-container>
        <v-row>
          <v-col md="4" v-for="(adoptado, i) in adoptados" :key="i">
            <Card :adoptado="adoptado" />
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<!-- Script -->
<script>
import Card from "@/components/adoption/Card.vue";
import { mapState } from "vuex";
export default {
  name: "Adoption",
  computed: {
    ...mapState(["adoptados"]),
  },
  components: {
    Card,
  },
};
</script>

<!-- Style -->
<style lang="scss">
.adoption {
  margin-bottom: 100px;
}
.banner-adoption {
  
  color: #ffffff;
  padding: 20px;
  text-shadow: 0.1em 0.1em #333;
  margin-bottom: 22px;
}
.cardsGroup {
  justify-content: center;
}
.introAdoption {
  background-color: #6b9cf7ec;
  color: #ffffff;
  text-align: left;
}
</style>
