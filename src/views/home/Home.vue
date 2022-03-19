<template>
  <v-container>
    <div class="my-6">
      <h2> Persist 2 variables from Vuex</h2>
      <p>
        <code>name</code> and <code>lastName</code> are persisted. <code> phone</code> is not.
      </p>
    </div>
 

    <v-row>
      <v-col sm="4">
        <small> Name</small>
        <v-text-field
          v-model="name"
          solo
        />
      </v-col>
      <v-col sm="4">
        <small> Lastname</small>
        <v-text-field
          v-model="lastName"
          solo
        />
      </v-col>
      <v-col sm="4">
        <small> Phone</small>
        <v-text-field
          v-model="phone"
          solo
        />
      </v-col>
    </v-row>
    </h3>
  </v-container>
</template>

  <script>
  import { sync} from 'vuex-pathify'
  export default {
    name: 'HomeView',
    computed: {
      ...sync('app' , [ 'name' , 'lastName']),
    },
  }
  </script>
