<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      app
      flat
      color="white"
      height="75"
      fixed
    >
      <v-toolbar-title>
        <h3>
          <nuxt-link :to="'/'" style="text-decoration: none; font-family: Arial; font-size: 25px;">Weather Today</nuxt-link>
        </h3>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn 
      :to="'/search'"
      depressed
      elevation="2"
      fab
      outlined
      raised
      rounded
      text
      color="white"
      >
        <v-icon color="blue">mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    search: null,
    searchClosed: true
  })
}
</script>

<style lang=sass>
  .v-input.expanding-search
    margin-top: 25px
    transition: max-width 0.3s
    .v-input__slot
      cursor: pointer !important
      &:before, &:after
        border-color: transparent !important
    &.closed
        max-width: 45px
        .v-input__slot
          background: transparent !important
</style>
