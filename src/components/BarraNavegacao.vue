<template >
    <nav class="navbar navbar-expand-lg navbar-bytebank">
      <a class="navbar-brand" href="#">ByteBank</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
       <BarraLogedIn v-if="usuarioestaLogado"/>
       <BarraNotLogedIn  v-else/>
     
      </div>
    </nav>
</template>
<script>
import BarraLogedIn from './BarraLogedIn.vue'
import BarraNotLogedIn from './BarraNotLogedIn.vue'

 export default {
  components: { BarraLogedIn, BarraNotLogedIn },
  computed: { 
    usuarioestaLogado () {
      return this.$store.getters.usuarioEstaLogado
    }
  }
 }
 </script>