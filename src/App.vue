<template>
  <v-app>
    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'


import * as Vue from 'vue' // in Vue 3
import axios from 'axios'

export default {
  name: 'App',
  methods: {
    getList() {
      this.axios.get(api).then((response) => {
        console.log(response.data)
      })
      // or
      this.$http.get(api).then((response) => {
        console.log(response.data)
      })
    }
  }
}
</script>
