<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center" id="titleBar">
        Mortgage Calculator
      </div>
    </v-app-bar>
    <v-content>
      <Home/>
    </v-content>
  </v-app>
</template>

<script>
import Home from './components/Home'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style lang="scss" scoped>
#titleBar {
  font-size: 1.5em;
  font-weight: 500;
}
</style>
