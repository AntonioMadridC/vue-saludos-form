<template>
  <div class="container">
    <h1>Formulario saludos</h1>
    <form class="row g-3" @submit.prevent="greet()">
      <div class="col-md-6">
        <label for="inputName" class="form-label">Nombres</label>
        <input type="text" class="form-control" id="inputName" v-model="name"/>
      </div>
      <div class="col-md-6">
        <label for="inputLastname" class="form-label">Apellidos</label>
        <input type="text" class="form-control" id="inputLastname" v-model="lastname"/>
      </div>
      <div class="col-md-6">
        <label for="inputEmail" class="form-label">Email</label>
        <input type="email" class="form-control" id="inputEmail" v-model="email"/>
      </div>
      <div class="col-md-6">
        <label for="inputAge" class="form-label">Edad</label>
        <input type="number" class="form-control" id="inputAge" v-model="age"/>
      </div>
      <div class="col-12">
        <button type="submit" class="btn btn-primary">Sign in</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "saludos-form",
  // props: {},
  data: function () {
    return {
        name: "",
        lastname: "",
        email: "",
        age: "",
    };
  },
  // computed: {},
  methods: {
    greet(){
        alert(`Saludos ${this.name} ${this.lastname}, tu correo es ${this.email}`)
        this.name = ""
        this.lastname = ""
        this.email = ""
        this.age = ""
    }
  }
  // watch: {},
  // components: {},
  // mixins: [],
  // filters: {},
  // -- Lifecycle Methods
  // -- End Lifecycle Methods
};
</script>

<style scoped>
</style>