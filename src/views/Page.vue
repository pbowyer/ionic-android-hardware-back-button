<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-menu-button color="primary"></ion-menu-button>
          <ion-back-button default-href="/"></ion-back-button>
        </ion-buttons>
        <ion-title>Page 1</ion-title>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true">
    
      <p>Just a bit of sample content. Carry on to the next page</p>
      <ion-button router-link="/page2">Go to Page 2</ion-button>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonButton, IonButtons, IonContent, IonHeader, IonMenuButton, IonPage, IonTitle, IonToolbar, IonBackButton } from '@ionic/vue';

export default {
  name: 'Folder',
  components: {
    IonButton,
    IonButtons,
    IonContent,
    IonHeader,
    IonMenuButton,
    IonPage,
    IonTitle,
    IonToolbar,
    IonBackButton
  }
}
</script>