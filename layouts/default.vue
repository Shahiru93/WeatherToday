<template>
  <v-app>
    <AppBar />
    <v-main>
      <v-conainer>
        <nuxt />
      </v-conainer>
    </v-main>
  </v-app>
</template>

<script>
import AppBar from '../components/AppBar'
export default {
  components: { AppBar }
}
</script>
