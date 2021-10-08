<template>
  <v-container>
    <v-row justify="center">
      <v-col>
        <h2>10:10 PM</h2>
        <h4>Friday, 08 October</h4>
        <h1>20&deg;C</h1>
      </v-col>
    </v-row>
    <v-row>
      <v-card elevation="3">
        <v-card-text>
          <v-col>
            <h5>Humidity : 58%</h5>
            <h5>Pressure : 10007hPa</h5>
            <h5>Wind Speed : 385m/s</h5>
            <h5>Sunrise : 06:00</h5>
            <h5>Sunset : 18:00</h5>
          </v-col>
        </v-card-text>
      </v-card>
    </v-row>
    <v-row class="mt-16">
      <v-slider
      v-model="time"
      :max="6"
      :tick-labels="labels"
      class="mx-4"
      ticks
    ></v-slider>
    </v-row>
    <v-row justify="center">
      <v-card align="center">
        <v-card-text>
          <v-col>
            <h4>Temperature</h4>
            <h1>Sri Lanka</h1>
            <p>
              <span class="headline">23&deg;</span>
              <span class="caption ml-2">cloudy</span>
            </p>
            <h5>Min-Max Temperature</h5>
            <h6>20&deg;C - 22&deg;C</h6>
          </v-col>
        </v-card-text>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      labels: ['SUN', 'MON', 'TUE', 'WED', 'THU', 'FRI', 'SA']
    }
  },
}
</script>