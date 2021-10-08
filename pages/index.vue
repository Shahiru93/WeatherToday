<template>
  <v-container fluid>
    <v-flex xs4>
      <h2>10:10 PM</h2>
      <h4>Friday, 08th Oct</h4>
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
    
    <v-flex mt-15>
      <v-card max-width="880" color="teal accent-1">
        <v-card-text>
          <v-row no-gutters>
            <v-card class="ma-3" xs-5 color="transparent" >
              <v-card-text>
                <h5>Monday</h5>
                <v-icon large>mdi-apple-icloud</v-icon>
                <h5>Night : 20&deg;C</h5>
                <h5>Day : 25&deg;C</h5>
              </v-card-text>
            </v-card>
            <v-card class="ma-3" xs-5 color="transparent" >
              <v-card-text>
                <h5>Monday</h5>
                <v-icon large>mdi-apple-icloud</v-icon>
                <h5>Night : 20&deg;C</h5>
                <h5>Day : 25&deg;C</h5>
              </v-card-text>
            </v-card>
            <v-card class="ma-3" xs-5 color="transparent" >
              <v-card-text>
                <h5>Monday</h5>
                <v-icon large>mdi-apple-icloud</v-icon>
                <h5>Night : 20&deg;C</h5>
                <h5>Day : 25&deg;C</h5>
              </v-card-text>
            </v-card>
            <v-card class="ma-3" xs-5 color="transparent" >
              <v-card-text>
                <h5>Monday</h5>
                <v-icon large>mdi-apple-icloud</v-icon>
                <h5>Night : 20&deg;C</h5>
                <h5>Day : 25&deg;C</h5>
              </v-card-text>
            </v-card>
            <v-card class="ma-3" xs-5 color="transparent" >
              <v-card-text>
                <h5>Monday</h5>
                <v-icon large>mdi-apple-icloud</v-icon>
                <h5>Night : 20&deg;C</h5>
                <h5>Day : 25&deg;C</h5>
              </v-card-text>
            </v-card>
            <v-card class="ma-3" xs-5 color="transparent" >
              <v-card-text>
                <h5>Monday</h5>
                <v-icon large>mdi-apple-icloud</v-icon>
                <h5>Night : 20&deg;C</h5>
                <h5>Day : 25&deg;C</h5>
              </v-card-text>
            </v-card>
            <v-card class="ma-3" xs-5 color="transparent" >
              <v-card-text>
                <h5>Monday</h5>
                <v-icon large>mdi-apple-icloud</v-icon>
                <h5>Night : 20&deg;C</h5>
                <h5>Day : 25&deg;C</h5>
              </v-card-text>
            </v-card>
          </v-row>
        </v-card-text>
      </v-card>
    </v-flex>
  </v-container>
</template>

<script>
export default {
  data () {
  },
  methods: {
    getWeatherInfo () {
      navigator.geolocation.getCurrentPosition((success) => {
        let {latitude, longitude} = sucsess.coords
      })
      this.$axios.$get(`https://api.openweathermap.org/data/2.5/onecall?lat=${latitude}&lon=${longitude}&exclude=hourly,minutely&appid=${API_KEY}`).then(res => (this.weather = res))
    },
  }
}
</script>