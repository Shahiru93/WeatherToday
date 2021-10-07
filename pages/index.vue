<template>
  <v-container fluid>
  </v-container>
</template>

<script>
  export default {
    data() {
      return {
        city: "London"
      }
    },
    created(){
      this.$axios.$get(`https://api.openweathermap.org/data/2.5/weather?q=${this.city}&129c5d65810fd42820964e446af9b61f`).then(res => console.log(res))
    }
  }
</script>
