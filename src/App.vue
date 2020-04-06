∑<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>Taste Profile</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn v-for="link in links" :key="`${link.label}-header-link`" text rounded :to="link.url">
        {{ link.label }}
      </v-btn>
    </v-app-bar>
    <v-content>
      <router-view></router-view>
    </v-content>
    <v-footer color="primary lighten-1" padless>
      <v-layout justify-center wrap>
        <v-btn
          v-for="link in links"
          :key="`${link.label}-footer-link`"
          color="white"
          text
          rounded
          class="my-2"
          :to="link.url"
        >
          {{ link.label }}
        </v-btn>
      </v-layout>
    </v-footer>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'App',
  data() {
    return {
      links: [
        {
          label: 'About',
          url: '/'
        },
        {
          label: 'Log in',
          url: '/login'
        },
        {
          label: 'Sign up',
          url: '/signup'
        }
      ]
    };
  }
});
</script>
