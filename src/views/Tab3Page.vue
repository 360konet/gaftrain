<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar color="">
        <ion-avatar class="center-image">
          <ion-img src="logo.png"></ion-img>
        </ion-avatar>
        <ion-title> My Profile</ion-title>
       </ion-toolbar>
      </ion-header>

      <div class="profile-container">
        <!-- User Profile Picture -->
        <ion-avatar class="profile-picture">
          <ion-img src="logo.png"></ion-img> <!-- Replace with your profile picture URL -->
        </ion-avatar>

        <ion-button>Edit Profile</ion-button>


        <!-- User Name -->
        <!-- <ion-title class="profile-name">John Doe</ion-title> -->

        <!-- User Information -->
        <div class="profile-info">
          <ion-label class="profile-name">Michael Kofi</ion-label>
          <ion-label>michael@gmail.com</ion-label>
          <ion-label>Col.</ion-label>          
          <ion-label>DIT</ion-label>
          <!-- Add more user information here -->
        </div>
      </div>

    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';
</script>

<style scoped>
.profile-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 16px;
}

.profile-picture {
  width: 120px;
  height: 120px;
}

.button{
  width: 120px;
  height: 20px;
  
}

.profile-name {
  font-size: 24px;
  font-weight: bold;
  margin-top: 8px;
}

.profile-info {
  margin-top: 16px;
  text-align: center;
}

.profile-info ion-label {
  display: block;
  margin-bottom: 8px;
}
</style>
