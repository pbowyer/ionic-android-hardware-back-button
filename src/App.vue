<template>
  <ion-app>
    <ion-router-outlet />
  </ion-app>
</template>

<script lang="ts">
import {IonApp, IonRouterOutlet, useBackButton, useIonRouter} from '@ionic/vue';
import { defineComponent } from 'vue';
import {useRouter} from 'vue-router';
import { Plugins } from "@capacitor/core";
const { App } = Plugins;

export default defineComponent({
  name: 'App',
  components: {
    IonApp,
    IonRouterOutlet
  },
  setup() {
    const ionRouter = useIonRouter();
    const router = useRouter();
    useBackButton(10, (processNextHandler) => {
      console.log("useBackButton handler was called!");
      if (ionRouter.canGoBack()) {
        console.log("Go back");
        router.back();
      } else {
        console.log("Exit app");
        App.exitApp();
      }
      processNextHandler();
    });
  }
});
</script>