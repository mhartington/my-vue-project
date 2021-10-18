<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Blank</ion-title>
          <ion-buttons slot="end">
            <ion-button>
              <ion-icon slot="icon-only" :icon="add"></ion-icon>
            </ion-button>
          </ion-buttons>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-item v-for="item in items" :key="item.id" :routerLink="'/detail/' + item.id">
          {{item.name}}
          <p slot="end">{{item.id}}</p>
      </ion-item>

    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonItem, IonButtons, IonButton, IonIcon } from '@ionic/vue';
import { add } from 'ionicons/icons';
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'Home',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonItem,
    IonButtons, IonButton, IonIcon
  },
  setup(){
    const items = ref([{name: 'foo', id: 1}])


    return { items, add }
  }
});
</script>

<style scoped></style>
