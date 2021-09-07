<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Datos Generales</div>
                    <div class="formulario mt-4 ml-4">
                         <form> <!--formulario datos generales-->
                            <div class="row">
                                <p class="Col-6">
                                    <label for="name">Nombre</label>
                                    <input
                                    id="name"
                                    v-model="nombre"
                                    type="text"
                                    name="name"
                                    >
                                </p>
                                <p class=col-6>
                                    <label for="name">Apellido</label>
                                    <input
                                    id="name"
                                    v-model="apellido"
                                    type="text"
                                    name="name"
                                    >
                                </p>
                            </div>
                            <div class="row">
                                <p>
                                    <label for="age">Fecha de Nacimiento</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="number"
                                    name="age"
                                    min="0">
                                </p>

                                <p>
                                    <label for="age">Edad</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="number"
                                    name="age"
                                    min="0">
                                </p>
                            </div>
                            <div class="row">
                                <p>
                                    <label for="age">Sexo</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="number"
                                    name="age"
                                    min="0">
                                </p>
                                <p>
                                    <label for="age">Codigo Postal</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="number"
                                    name="age"
                                    min="0">
                                </p>
                            </div>
                            <div class="row">
                            </div>
                            <div class="col-12">
                                <p>
                                    <label for="age">Domicilio</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="number"
                                    name="age"
                                    min="0">
                                </p>
                            </div>
                            <div class="row">
                                <p>
                                    <label for="age">Ciudad</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="number"
                                    name="age"
                                    min="0">
                                </p>
                                <p>
                                    <label for="movie">Estado</label>
                                    <select
                                    id="movie"
                                    v-model="movie"
                                    name="movie"
                                    >
                                    <option>Star Wars</option>
                                    <option>Vanilla Sky</option>
                                    <option>Atomic Blonde</option>
                                    </select>
                                </p>
                            </div>
                            <div class="row">
                                <p>
                                    <label for="age">Celular</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="number"
                                    name="age"
                                    min="0">
                                </p>
                                <p>
                                    <label for="age">Telefono</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="number"
                                    name="age"
                                    min="0">
                                </p>
                            </div>
                            <div class="col-12">
                                <p>
                                    <label for="age">Tutor</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="text"
                                    name="age"
                                    min="0">
                                </p>
                            </div>
                            <div class="row">
                                <p>
                                    <label for="age">Telefono</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="text"
                                    name="age"
                                    min="0">
                                </p>
                                <p>
                                    <label for="age">Teléfono extra</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="text"
                                    name="age"
                                    min="0">
                                </p>
                            </div>
                            <div class="col-12">    
                                <p>
                                    <label for="age">Dirección</label>
                                    <input
                                    id="age"
                                    v-model="age"
                                    type="text"
                                    name="age"
                                    min="0">
                                </p>
                            </div>
                        </form>
                    </div>
                </div>
                <div class="card">
                    <div class="card-header">Información de Ortodoncista</div>        
                    
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        },
        data(){
          return{
              nombre:"",
              apellido:"",
              fechaNac:"",
              edad:"",
              sexo:"",
              domicilio:"",
              ciudad:"",
              estado:"",
              codigopostal:"",
              celular:"",
              telefono:"",
              email:"",
              tutor:"",
              telefonotutor:"",
              telefonotutor2:"",
              direcciontutor:"",
         }
         },
    }
</script>

