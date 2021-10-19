<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Home</ion-title>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true">
      <h3>1. Test the back button</h3>
      <p>Start the app. Press the button below until you come to Page 2. Then try the Android back button.</p>
      <p><strong>It should:</strong> take you to Page 1. And if pressed again to Home.</p>
      <p><strong>It does:</strong> go all the way back to Home.</p>
      <ion-button router-link="/page1">Go to Page 1</ion-button>

      <h3>2. Test exiting the app immediately [works]</h3>
      <p>Restart the app. Press the Android back button immediately. The app should exit/go into the background.</p>

      <h3>3. Test exiting the app after navigating</h3>
      <p>Restart (or bring to the foreground?) the app. Navigate through to Page 2. Press the Android back button until you come back to Home. Press again</p>
      <p><strong>It should:</strong> exit/put the app in the background.</p>
      <p><strong>It does:</strong> nothing.</p>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {IonButton, IonContent, IonHeader, IonPage, IonTitle, IonToolbar} from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Home',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonButton
  }
});
</script>