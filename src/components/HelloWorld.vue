<template>
  <div>
      <v-btn @click="alertDisplay">Hello world</v-btn>
        <b-button  @click="alertDisplay" variant="primary">Primary</b-button>
    <b-table striped hover :items="items"></b-table>
  </div>
</template>

<script>
  export default {
    data() {
      return {
         text: '',
        items: [
          { age: 40, first_name: 'Dickerson', last_name: 'Macdonald' },
          { age: 21, first_name: 'Larsen', last_name: 'Shaw' },
          { age: 89, first_name: 'Geneva', last_name: 'Wilson' },
          { age: 38, first_name: 'Jami', last_name: 'Carney' }
        ]
      }
    },
     methods: {
      alertDisplay() {
        // $swal function calls SweetAlert into the application with the specified configuration.
        this.$swal('Heading', 'this is a Heading', 'OK');
      }
    }
  }
</script>