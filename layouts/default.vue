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
          <nuxt-link :to="'/'" style="text-decoration: none; color: blue; font-family: Arial; font-size: 25px;">Weather Today</nuxt-link>
        </h3>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-text-field
      @focus="searchClosed = false"
      @blur="searchClosed = true"
      v-model="search"
      placeholder="Search..."
      prepend-inner-icon="mdi-magnify"
      class="expanding-search"
      :class="{ 'closed' : searchClosed && !search }"
      filled
      dense
      clearable
      ></v-text-field>
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
