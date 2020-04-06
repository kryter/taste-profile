<template>
  <v-card class="login page mx-auto mt-5 mb-5" width="400">
    <v-card-title>
      <h1 class="display-1">Log in</h1>
    </v-card-title>
    <v-card-text>
      <v-form>
        <v-text-field label="Username" prepend-icon="mdi-account-circle" />
        <v-text-field
          :type="showPassword ? 'text' : 'password'"
          label="Password"
          prepend-icon="mdi-lock"
          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
          @click:append="showPassword = !showPassword"
        />
      </v-form>
    </v-card-text>
    <v-divider></v-divider>
    <v-card-actions>
      <v-btn color="success">Sign up</v-btn>
      <v-spacer></v-spacer>
      <v-btn color="info">Log in</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script lang="ts">
export default {
  name: 'LoginPage',
  data() {
    return {
      showPassword: false
    };
  }
};
</script>

<style></style>
