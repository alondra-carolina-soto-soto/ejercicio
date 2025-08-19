<template>
  <div class="contenedor">
  <div class="hello">
    <h1 class="animate__animated animate__bounceInDown msg">{{ msg }}</h1>
    <h3 class="animate__animated animate__flash type">ALONDRA CAROLINA SOTO SOTO</h3>
    <div class="mb-3">
  <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="escribe...">
</div>
  
    <button class="btn btn-warning" @click="mostrarMensaje">Warning</button>
    <p v-if="mensajeVisible" class="animate__animated animate__fadeInDown">ejercicio previo al examen</p>
    </div>
  </div>
      <footer class="footer">
  <div class="footer-left">Desarrollo Web integral</div>
  <div class="footer-center">Universidad Tecnológica de Del Mezquital</div>
  <div class="footer-right"> 10°Cuatrimestre 2025</div>
</footer>

</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      mensajeVisible: false
    };
  },
  methods: {
    mostrarMensaje() {
      this.mensajeVisible = true;
    }
  }
};
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}


.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #f0f0f0;
  padding: 10px 20px;
  font-size: 14px;
  margin-top: 30px;
  border-top: 1px solid #ccc;
}

.footer-left {
  text-align: left;
  flex: 1;
}

.footer-center {
  text-align: center;
  flex: 1;
}

.footer-right {
  text-align: right;
  flex: 1;
}
.contenedor {
  display: flex;
  flex-direction: column;
  min-height: 100vh; /* altura completa de la pantalla */
}

.hello {
  flex: 1; /* ocupa el espacio disponible arriba del footer */
}
</style>
