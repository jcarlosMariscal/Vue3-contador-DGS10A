<!-- VUE.js SFC - Single File Component 
  JS-script 
  CSS-style 
  HTML-template 
  contador: 0; 
  contador++;

<script></script> -->
<script>
// export default {
//   data(){
//     return{
//       contador: 200,
//     };
//   },
// };
export default {
  data: () => ({
    contador: 500,
  }),
  methods: {
    saludar() {
      console.log("Hola 10A");
    },
    incrementar() {
      this.contador++;
    },
    decrementar() {
      this.contador--;
    },
    resetear() {
      this.contador = 0;
    },
  },
};
</script>

<template>
  <img src="./assets/logo.svg" alt="Logo Vue" width="125" height="125" />

  <div class="container">
    <small>
      <h1>Hola desde VUE.js 3, Cambios desde local</h1>
    </small>
    <br />
    <h2>Contador {{ contador }}</h2>
    <br />
    <button @click="incrementar()">+1</button>
    <button @click="decrementar()">-1</button>
    <button @click="resetear()">Reset</button>
    <!-- Button trigger modal -->
    <button
      type="button"
      class="btn-m"
      data-toggle="modal"
      data-target="#modal"
    >
      Open
    </button>
  </div>
  <!-- Modal -->
  <div class="modal fade" id="modal" tabindex="-1" role="dialog">
    <div class="modal-dialog" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel">
            Juan Carlos Ramírez Mariscal - DGS - 10A
          </h5>
        </div>
        <div class="modal-body">
          <span>VUE Deploy: Netlify, Vercel y GitHub</span>
          <span>Clase 9 de septiembre de 2022</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  text-align: center;
}
small {
  color: #666;
}
h1 {
  font-weight: bolder;
}
h2 {
  font-size: 2.5rem;
}
button {
  cursor: pointer;
  font-size: 1.5rem;
  margin: 0px 8px;
}

h5 {
  color: #34495e;
}
span {
  color: #34495e;
}
</style>
