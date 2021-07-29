<template>
  <ion-app>
    <ion-menu side="start" content-id="main-content">
      <ion-header>
        <ion-toolbar translucent>
          <ion-title>Menu</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content>
        <ion-list>
          <ion-item button @click="buttonClick()">
            <ion-icon :icon="heart" slot="start"></ion-icon>
            <ion-label>Inbox</ion-label>
          </ion-item>
          <ion-item>
            <ion-icon name="paper-plane" slot="start"></ion-icon>
            <ion-label>Outbox</ion-label>
          </ion-item>
          <ion-item>
            <ion-icon name="heart" slot="start"></ion-icon>
            <ion-label>Favorites</ion-label>
          </ion-item>
          <ion-item>
            <ion-icon name="archive" slot="start"></ion-icon>
            <ion-label>Archived</ion-label>
          </ion-item>
          <ion-item>
            <ion-icon name="trash" slot="start"></ion-icon>
            <ion-label>Trash</ion-label>
          </ion-item>
          <ion-item>
            <ion-icon name="warning" slot="start"></ion-icon>
            <ion-label>Spam</ion-label>
          </ion-item>
        </ion-list>
      </ion-content>
    </ion-menu>
    <ion-router-outlet id="main-content" />
  </ion-app>
</template>

<script lang="ts">
import { 
  IonApp, 
  IonRouterOutlet, 
  IonContent, 
  IonHeader, 
  IonItem, 
  IonList, 
  IonMenu, 
  IonTitle, 
  IonToolbar,
  IonIcon,
  IonLabel
} from '@ionic/vue';
import { heart } from 'ionicons/icons';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'App',
  components: {
    IonApp,
    IonRouterOutlet,
    IonContent, 
    IonHeader, 
    IonItem, 
    IonList, 
    IonMenu, 
    IonTitle, 
    IonToolbar,
    IonIcon,
    IonLabel
  },
  setup(){
    return { heart  }
  },
  methods: {
    buttonClick() {
      // Vueはmethodsのthisを自動的に束縛して、常にコンポーネントのインスタンスを参照します。
      // これにより、メソッドがイベントリスナやコールバックとして使われる際に、正しいthisの値を保持することができます。
      // Vueが適切なthisの値を束縛するのを防ぐため、methodsを定義する際にはアロー関数を使うのは避けるべきです。
      console.log("aaaa")
    }
  }
});
</script>