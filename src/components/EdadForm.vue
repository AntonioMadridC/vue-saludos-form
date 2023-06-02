<template>
  <div class="container">
    <h1>Formulario grupo etario</h1>
    <form class="row g-3 m-5" @submit.prevent="stage()">
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
  name: "edad-form",
  // props: {},
  data: function () {
    return {
        age: ""
    };
  },
  // computed: {},
  methods: {
    stage(){
        let age = this.age
        if (age<13) {
            alert("Su etapa es niñez")
        } else {
            if (age<18) {
                alert("Su etapa es adolescencia")
            } else {
                if (age<36) {
                    alert("Su etapa es adulo joven")
                } else {
                    if (age<65) {
                        alert("Su etapa es adulto")
                    } else {
                        alert("Su etapa es tercera edad")
                    }
                }
            }
        }
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