<template>
    <v-container>
            <v-flex xs12>
                <v-card color="blue" dark>
                    <v-card-text>
                        <v-layout v-if="weather.weather" justify-center>
                            <v-flex class="text-xs-center">
                                <h4>Temperature</h4>
                                <h1 class="display-1">{{ weather.name }}</h1>
                                <img :src="icon" alt="weather icon">
                                <p>
                                    <span class="dispaly-1">{{ temp() }} &#176;C</span>
                                </p>
                            </v-flex>
                        </v-layout>
                    </v-card-text>
                </v-card>
            </v-flex>
            <v-flex xs12 class="mt-4">
                <v-form @submit.prevent="getWeatherInfo">
                <v-text-field label="Enter City Name..." solo v-model="city"></v-text-field>
                </v-form>
            </v-flex>
    </v-container>
</template>

<script>
export default {
    data () {
        return {
            city : 'London',
            weather: {}
        }
    },
    created () {
        this.getWeatherInfo ()
    },
    computed:{
        icon () {
            return this.weather.weather ? `https://openweathermap.org/img/w/${this.weather.weather[0].icon}.png`:''
        }
    },
    methods: {
        getWeatherInfo () {
            this.$axios.$get(`https://api.openweathermap.org/data/2.5/weather?q=${this.city}&appid=129c5d65810fd42820964e446af9b61f`).then(res => (this.weather = res))
        },
        temp () {
            return this.weather.main ? Math.round(this.weather.main.temp - 273) : ''
    }
    }
    
}
</script>