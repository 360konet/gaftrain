<template>
    <ion-page>
      <ion-header>
        <ion-toolbar>
          <ion-title>Register</ion-title>
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
            <ion-label position="floating">Service Number</ion-label>
            <ion-input type="email"></ion-input>
          </ion-item>
  
          <div class="ion-row">
            <ion-col size="6">
              <ion-item>
                <ion-label position="floating">Rank</ion-label>
                <ion-input type="text"></ion-input>
              </ion-item>
            </ion-col>
            <ion-col size="6">
              <ion-item>
                <ion-label position="floating">Name</ion-label>
                <ion-input type="text"></ion-input>
              </ion-item>
            </ion-col>
          </div>
  
          <div class="ion-row">
            <ion-col size="6">
              <ion-item>
                <ion-label position="floating">Password</ion-label>
                <ion-input type="password"></ion-input>
              </ion-item>
            </ion-col>
            <ion-col size="6">
              <ion-item>
                <ion-label position="floating">Confirm Password</ion-label>
                <ion-input type="password"></ion-input>
              </ion-item>
            </ion-col>
          </div>
  
          <ion-button expand="full" @click="register">Register</ion-button>
          <router-link to="/login">Register</router-link>
          <div class="register-link">
            Already having an account? <router-link to="/login">Login</router-link>
          </div>
        </div>
      </ion-content>
    </ion-page>
  </template>
  
  <script setup lang="ts">
  import { ref } from 'vue';
  import { useRouter } from 'vue-router';
  import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonItem, IonInput, IonButton, IonCol } from '@ionic/vue';
  
//   const email = ref('');
//   const name = ref('');
//   const rank = ref('');
//   const password = ref('');
//   const confirmPassword = ref('');
  
  const register = () => {
    const router = useRouter();
    router.push('/login');
  };
  </script>
  
  <style scoped>
  .registration-form {
    display: flex;
    flex-direction: column;
  }
  
  .ion-row {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  
  .ion-col {
    flex: 1;
    margin-right: 8px; /* Add spacing between columns */
  }

  .login-logo {
    width: 100px;
    height: 100px;
    margin-bottom: 16px;
    align-items: center;
    justify-content: center;
  }

  .login-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
  }
  </style>
  