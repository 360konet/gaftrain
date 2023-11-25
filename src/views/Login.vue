<template>
    <ion-page>
      <ion-header>
        <ion-toolbar>
          <ion-title>Login</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content class="ion-padding">
        <div class="login-container">
          <ion-img src="logo.png" class="login-logo"></ion-img> <!-- Replace with your logo image -->
          <ion-item>
            <ion-label position="floating">Email</ion-label>
            <ion-input type="email"></ion-input>
          </ion-item>
          <ion-item>
            <ion-label position="floating">Password</ion-label>
            <ion-input type="password"></ion-input>
          </ion-item>
          <ion-button expand="full" @click="openNewPage">Login</ion-button>
          <router-link to="/tabs/tab1">Login</router-link>
          <div class="register-link">
            Don't have an account? <router-link to="/register">Register</router-link>
          </div>
        </div>
      </ion-content>
    </ion-page>
  </template>
  
  <script setup lang="ts">
  import { useRouter } from 'vue-router';
  
  const openNewPage = () => {
    const router = useRouter();
    router.push('/register'); // Replace '/new-page' with the desired route path
  };
  </script>
  
  <style scoped>
  .login-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
  }
  
  .login-logo {
    width: 100px;
    height: 100px;
    margin-bottom: 16px;
  }
  
  .register-link {
    margin-top: 16px;
    text-align: center;
  }
  </style>
  