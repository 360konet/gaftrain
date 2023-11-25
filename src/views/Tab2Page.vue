<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar color="">
        <ion-avatar class="center-image">
          <ion-img src="logo.png"></ion-img>
        </ion-avatar>
        <ion-title>My Records</ion-title>
       </ion-toolbar>
      </ion-header>
      <ion-header collapse="condense">
      </ion-header>

      <div class="record-table">
        <div class="record-row header">
          <div class="record-cell">Date</div>
          <div class="record-cell">Time</div>
          <div class="record-cell">Duration</div>
        </div>

        <!-- Example Record Rows -->
        <div class="record-row">
          <div class="record-cell">2023-09-05</div>
          <div class="record-cell">14:30:45</div>
          <div class="record-cell">00:30:15</div>
        </div>
        <div class="record-row">
          <div class="record-cell">2023-09-04</div>
          <div class="record-cell">16:15:20</div>
          <div class="record-cell">00:45:30</div>
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
.record-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 16px;
}

.record-row {
  display: flex;
  justify-content: space-between;
  border: 1px solid #ccc;
  padding: 8px;
}

.record-cell {
  flex: 1;
  text-align: center;
  padding: 8px;
  border-right: 1px solid #ccc;
}

.record-cell:last-child {
  border-right: none;
}

.header {
  background-color: #333;
  color: #fff;
  font-weight: bold;
}
</style>
