∑<template>
  <v-app>
    <Navbar />
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';
import Navbar from './components/Navbar.vue';

@Component({
  name: 'App',
  components: {
    Navbar
  }
})
export default class App extends Vue {}
</script>
