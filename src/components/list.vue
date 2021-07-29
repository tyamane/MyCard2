<template>
  <!-- List of Text Items -->
  <ion-list>
    <ion-item v-for="item in listItem" v-bind:key="item.id">
      <ion-icon :icon="cloudyOutline" slot="start"></ion-icon>
      <ion-label>{{item.name}}</ion-label>
    </ion-item>

<!--
    <ion-item>
      <ion-label>Pokemon Yellow</ion-label>
    </ion-item>
    <ion-item>
      <ion-label>Mega Man X</ion-label>
    </ion-item>
    <ion-item>
      <ion-label>The Legend of Zelda</ion-label>
    </ion-item>
    <ion-item>
      <ion-label>Pac-Man</ion-label>
    </ion-item>
    <ion-item>
      <ion-label>Super Mario World</ion-label>
    </ion-item>
-->    
  </ion-list>

</template>

<script lang="ts">
import {defineComponent} from 'vue';
import { cloudyOutline } from 'ionicons/icons';
import { 
  IonList,
  IonItem, 
  IonIcon,
  IonLabel
} from '@ionic/vue';
interface Coupon{
  id: number;
  name: string;
}
export default defineComponent({
    name: "list",
    components:{
      IonList,
      IonIcon,
      IonItem,
      IonLabel
    },
    setup(){
      const listItem: Array<Coupon> = [
        {id: 1, name: "Pokemon Yellow"},
        {id: 2, name: "Mega Man X"},
        {id: 3, name: "The Legend of Zelda"},      
        {id: 4, name: "Pac-Man"},  
        {id: 5, name: "Super Mario World"}
      ];
      const msg = "Hello";
      return {listItem, msg, cloudyOutline}
    }
});
</script>