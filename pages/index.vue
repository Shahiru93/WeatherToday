<template>
  <v-container fluid>
    <v-flex xs4>
      <h2>10:10 PM</h2>
      <h4>Friday, 08th Oct</h4>
      <h1>30&deg;C</h1>
      <v-icon large>mdi-apple-icloud</v-icon>
    </v-flex>
    <v-card max-width="200" color="cyan darken-4" dark>
      <v-card-text>
        <v-flex>
          <h5 class="caption">Sunrise : 05:00 AM</h5>
          <h5 class="caption">Sunset : 06:00 PM</h5>
          <h5 class="caption">Humidity : 50%</h5>
          <h5 class="caption">Winds Speed : 200&deg;</h5>
        </v-flex>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        labels: ['SUN', 'MON', 'TUE', 'WED', 'THU', 'FRI', 'SAT']
      }
    }
  }
</script>