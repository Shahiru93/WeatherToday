<template>
  <v-app>
    <AppBar />
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import AppBar from '../components/AppBar'
export default {
  components: { AppBar }
}
</script>
