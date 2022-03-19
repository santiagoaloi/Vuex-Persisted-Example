<template>
  <v-app-bar app>
    <v-toolbar-title>Persist Vuex state with <code> VuexPersist </code> and <code> localForage</code></v-toolbar-title>
  </v-app-bar>
</template>

<script>
  // Utilities
  import { sync } from 'vuex-pathify'

  export default {
    name: 'DefaultAppBar',
    computed: { drawer: sync('app/drawer') },
  }
</script>
