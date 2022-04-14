<!-- Template -->
<template>
  <div>
    <div class="banner-about">
      <h1 id="tituloMision"></h1>
    </div>
    <div class="contMision">
      <b-container class="txtPrincipal p-5">
        N replicant adopciones y informacion de mascotas 
      </b-container>

      <b-container>
        <b-row>
          <b-col class="contCorgi p-5">
            <img
              src="http://www.cuentoscortos.com/imagenes/2587-grande.jpg"
              img-alt="Card image"
              class="imgCorgiRoyale"
            />
          </b-col>
          <b-col class="txtRaza p-5">
            RECUERDA QUE UN PERRITO ES PARA TODA LA VIDA Y NO SOLO PARA CUANDO ES CACHORRO...
          </b-col>
        </b-row>
      </b-container>

      <b-container>
        <b-row>
          <b-col class="txtPrimero p-5">
           CADA PERRITO ES ESPECIAL Y TE ENTREGARA AMOR ETERNO 
          </b-col>
          <b-col class="txtSegundo p-5">
           UNA VEZ QUE LLEGA  A TU VIDA JAMAS SE SEPARARA DE TI Y TE VERA COMO SU AMO 
          </b-col>
        </b-row>
      </b-container>

      <b-container>
        <b-row>
          <b-col class="contMestizo p-5">
            <img
              src="https://scontent.fscl8-1.fna.fbcdn.net/v/t1.6435-9/52591506_2400586056619756_3379548957351870464_n.jpg?_nc_cat=105&ccb=1-5&_nc_sid=730e14&_nc_ohc=hqXIIxNgOK0AX-nnZ6b&_nc_ht=scontent.fscl8-1.fna&oh=00_AT-TEVy6wABG-HcbpGAofb4dfMr8hqkBZXXTnc-GI2scQQ&oe=627C51AA"
              img-alt="Card image"
              class="imgMestizo"
            />
          </b-col>
          <b-col class="txtMestizo p-5">
            NUNCA TE TRAICIONARA ASI QUE NO SE LO HAGAS A EL
          </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<!-- Script -->
<script>
export default {};
</script>

<!-- Style -->
<style lang="scss">
.about {
  margin-bottom: 100px;
}
.banner-about {
  
  color: #ffffff;
  padding: 20px;
  text-shadow: 0.1em 0.1em #333;
  margin-bottom: 22px;
}
.contMision {
  margin-bottom: 100px;
}
.txtPrincipal {
  background-color: #f36bbfde !important;
  color: #ffffff;
  text-align: left;
}
.txtRaza {
  text-align: justify;
}
.txtPrimero {
  background-color: rgb(149, 115, 228);
  color: #ffffff;
  text-align: justify;
}
.txtSegundo {
  background-color: rgb(99, 51, 211);
  color: #ffffff;
  text-align: justify;
}
.txtMestizo {
  text-align: justify;
}
.imgCorgiRoyale {
  max-width: 50%;
}
.imgMestizo {
  max-width: 50%;
}
@media (max-width: 768px) {
  .contCorgi {
    display: none;
  }
  .contMestizo {
    display: none;
  }
}
</style>
