<template>
  <ion-page class="login-page">
    <ion-header translucent>
      <ion-toolbar>
        <ion-title>Login</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content class="ion-padding">
      <div class="login-container">
        <h1>Welcome Back</h1>
        <form @submit.prevent="handleLogin">
          <ion-item>
            <ion-label position="floating">Email</ion-label>
            <ion-input type="email" v-model="email" required></ion-input>
          </ion-item>
          <ion-item>
            <ion-label position="floating">Password</ion-label>
            <ion-input type="password" v-model="password" required></ion-input>
          </ion-item>
          <ion-button expand="full" type="submit">Login</ion-button>
        </form>
        <p class="register-link">Don't have an account? <a href="/register">Register here</a></p>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const email = ref('');
const password = ref('');

const handleLogin = () => {
  // Handle login logic here
  console.log('Logging in with:', email.value, password.value);
};
</script>

<style scoped>
.login-page {
  background-color: #f9f9f9;
}

.login-container {
  max-width: 400px;
  margin: auto;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  background-color: white;
}

.login-container h1 {
  text-align: center;
  margin-bottom: 20px;
}

.register-link {
  text-align: center;
  margin-top: 15px;
}

.register-link a {
  color: #007bff;
  text-decoration: none;
}
</style>