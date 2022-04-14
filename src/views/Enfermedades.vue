<!-- Template -->
<template>
  <div>
    <div class="banner-tips">
      <h1>Enfermedades Genéticas</h1>
    </div>

    <b-container class="introEnfermedades p-5">
     Enfermedades más comunes en perros
A continuación te mostramos cuáles son las enfermedades y la forma de tratarlas, más comunes en perros de cualquier raza o edad.

Moquillo
Esta enfermedad es muy contagiosa en perros, generado por un virus similar al del sarampión. Se previene mediante vacunación y, en caso de infección, el tratamiento se basa en la administración de antibióticos y cuidar de que nuestro compañero se mantenga en todo momento hidratado.
Leptospirosis
Causada por una bacteria llamada espiroqueta se contagia a través del contacto con orina de un perro infectado o a través de la piel, por una herida. La mayoría de los casos no reviste gravedad y puede tratarse con antibióticos.
Parvovirus
Una enfermedad con una gran tasa de contagio que ataca las células que se reproducen en el tracto intestinal. Se propaga mediante las heces y puede prevenirse con su correspondiente vacuna.

Diarrea en perros
Las causas por las que un perro puede tener deposiciones líquidas pueden ser diferentes. Generalmente puede deberse a un cambio de alimentación, una alergia alimentaria o incluso por infección de parásitos intestinales. La diarrea puede ser aguda, de corta o media duración y crónica, que necesitará de una visita al veterinario para determinar el origen.

Alergias cutáneas
Las alergias son una enfermedad de las más comunes en perros y suelen ser de origen cutáneo. Deberemos realizar una visita al veterinario para determinar cuál es la causa y suministrarle antihistamínicos de ser necesario.

¿Por qué es tan importante vacunar a tu perro?
Con las vacunas al día de tu perro tendrás la seguridad de prevenir alguna de estas y otras enfermedades más comunes. Hemos hablado de algunas enfermedades, pero existen muchas más que pueden ser evitadas con la vacunación anual.

Consejos a tener en cuenta para la vacunación de tu perro
No vacunar a nuestro compañero puede tener un coste mucho más alto al tratar la enfermedad del mismo. La vacunación y desparasitación es más económico previniendo la mayoría de las enfermedades y sus posibles secuelas.

En los primeros cuatro meses de vida de tu perro es importante reforzar la salud de tu perro con algunos complementos. Pedir consejo a tu veterinario es importante ya que él dictará las pautas a seguir. Nunca se debe vacunar a un perro que esté padeciendo algún tipo de enfermedad, sobre todo, si su sistema inmunológico se encuentra afectado ya que puede agravar su estado de salud.

Vacunas recomendadas para perros
La rabia es una vacuna obligatoria por la legislación vigente, ésta debe ser suministrada en el tercer mes de edad y repetirse al cabo del mes. Posteriormente, se vacunará al animal cada año. El resto de vacunas recomendadas son la de hepatitis infecciosa, moquillo, parvovirus, leptospirosis y traqueobronquitis infecciosa.
    </b-container>

    <div class="tips container">
      <v-container>
        <v-row>
          <v-col md="4" v-for="(tip, i) in tips" :key="i">
            <Cardtips :tip="tip" />
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<!-- Script -->
<script>
import { mapState } from "vuex";
import Cardtips from "@/components/enfermedades/Cardtips.vue";
export default {
  name: "Enfermedades",
  components: {
    Cardtips,
  },
  computed: {
    ...mapState(["tips"]),
  },
};
</script>

<!-- Style -->
<style lang="scss">
.tips {
  margin-bottom: 100px;
}
.banner-tips {
 
  color: #ffffff;
  padding: 20px;
  text-shadow: 0.1em 0.1em #333;
  margin-bottom: 22px;
}
.introEnfermedades {
  background-color: #4a70ecc7;
  color: #ffffff;
  text-align: justify;
}
</style>
