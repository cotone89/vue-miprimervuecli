<template>
    <div id="app">
        <h1 class="text-center">{{titulo}}</h1>
        <table class="table">
            <thead>
                <tr>
                    <th scope="col">#</th>
                    <th scope="col">Nombre</th>
                    <th scope="col">Apellido</th>
                    <th scope="col">Run</th>
                    <th scope="col">Nacimiento</th>
                    <th scope="col">Edad</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(usuario, index) of usuarios" v-bind:key="index">
                    <th scope="row">{{index+1}}</th>
                    <td>{{usuario.nombre}}</td>
                    <td>{{usuario.apellido}}</td>
                    <td>{{usuario.run}}</td>
                    <td>{{usuario.nacimiento}}</td>
                    <td>{{usuario.edad}}</td>
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
                titulo: 'Tabla de Usuarios',
                usuarios: [{
                    'nombre': 'nombre1',
                    'apellido': 'apellido1',
                    'run': 'run1',
                    'nacimiento': 'nacimiento1',
                    'edad': 'edad1'
                },
                {
                    'nombre': 'nombre2',
                    'apellido': 'apellido2',
                    'run': 'run2',
                    'nacimiento': 'nacimiento2',
                    'edad': 'edad2'
                },
                {
                    'nombre': 'nombre3',
                    'apellido': 'apellido3',
                    'run': 'run3',
                    'nacimiento': 'nacimiento3',
                    'edad': 'edad3'
                }
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
</style>
