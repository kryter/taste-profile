∑<template>
  <v-app-bar app color="primary" dark>
    <v-toolbar-title>Taste Profile</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-btn v-for="link in links" :key="`${link.label}-header-link`" text rounded :to="link.url">{{
      link.label
    }}</v-btn>
  </v-app-bar>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';

export interface LinkData {
  label: string;
  url: string;
}

@Component({
  name: 'Navbar'
})
export default class Navbar extends Vue {
  private static linksBeforeSignIn = [
    {
      label: 'About',
      url: '/'
    },
    {
      label: 'Sign up',
      url: '/signup'
    },
    {
      label: 'Log in',
      url: '/login'
    }
  ];

  private links: LinkData[] = Navbar.linksBeforeSignIn;
}
</script>
