<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1 class="text-center">Tabla de Usuarios</h1>
        <table class="table table-striped">
            <thead>
                <tr>
                    <th>#</th>
                    <th>Nombre</th>
                    <th>Apellido</th>
                    <th>RUN</th>
                    <th>Nacimiento</th>
                    <th>Edad</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(datos, index) in datos" :key="datos.datos">
                    <th scope="row">{{ index + 1 }}</th>
                    <td>{{ datos.nombre }}</td>
                    <td>{{ datos.apellido }}</td>
                    <td>{{ datos.run }}</td>
                    <td>{{ datos.nacimiento }}</td>
                    <td>{{ datos.edad }}</td>
                </tr>
            </tbody>
        </table>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      datos: [
        { nombre: "Jose", apellido: "Pérez", run: "123456-2", nacimiento: "12-04-67", edad: 52 },
        { nombre: "María", apellido: "Rodríguez", run: "654321-1", nacimiento: "30-11-90", edad: 29 },
        { nombre: "Cristopher", apellido: "Muñoz", run: "16999666-8", nacimiento: "15-04-88", edad: 33 },
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.text-center {
  margin-top: 60px;
}
</style>
