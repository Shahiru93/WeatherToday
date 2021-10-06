<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      app
      color="#"
      height="75"
      fixed
    >
      <v-toolbar-title>
        <h3>
          <nuxt-link :to="'/'" style="text-decoration: none;">Weather Today</nuxt-link>
        </h3>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-text-field
      @focus="searchClosed = false"
      @blur="searchClosed = true"
      placeholder="Search..."
      prepend-inner-icon="mdi-magnify"
      class="expanding-search mt-2"
      :class="{ 'closed' : searchClosed }"
      filled
      dense
      ></v-text-field>
    </v-app-bar>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    searchClosed: true
  })
}
</script>

<style lang=sass>
  .v-input.expanding-search
    transition: max-width 0.3s
    .v-input__slot
      &:before, &:after
        border-color: transparent !important
    &.closed
        max-width: 45px
</style>
