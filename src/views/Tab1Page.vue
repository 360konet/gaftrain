<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar color="">
          <ion-avatar class="center-image">
            <ion-img src="logo.png"></ion-img>
          </ion-avatar>
          <ion-title>GAF FIT</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large"></ion-title>
        </ion-toolbar>
      </ion-header>

      <div class="circle-button-container">
        <ion-button fill="outline" class="start-button">Start</ion-button>
        <div class="time-label-container">
          <ion-label class="stopwatch">{{ formattedTime }}</ion-label>
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';

import { ref, computed } from 'vue';

const startTime = ref(0);
const timerInterval = ref<number | null>(null); // Change the type to number | null

const formattedTime = computed(() => {
  const currentTime = Date.now() - startTime.value;
  const hours = Math.floor(currentTime / 3600000);
  const minutes = Math.floor((currentTime % 3600000) / 60000);
  const seconds = Math.floor((currentTime % 60000) / 1000);
  const milliseconds = (currentTime % 1000).toString().slice(0, 2);

  return `${String(hours).padStart(2, '0')}:${String(minutes).padStart(2, '0')}:${String(seconds).padStart(2, '0')}:${milliseconds}`;
});

</script>

<style scoped>
.circle-button-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 70vh;
}

.profile-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin-top: 16px;
}

.start-button {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  font-size: 18px;
  --border-radius: 50%;
}

.center-image {
  display: flex;
  justify-content: center;
  align-items: center;
}

.stopwatch {
  margin-top: 16px;
  font-size: 24px;
}
</style>
