<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Detail</ion-title>

        <ion-buttons slot="start">
            <ion-back-button defaultHref="/"></ion-back-button>
        </ion-buttons>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Detail</ion-title>
        </ion-toolbar>
      </ion-header>
        <p>My dynamic id = {{ id }}</p>

    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonButtons, IonBackButton  } from '@ionic/vue';
import { add } from 'ionicons/icons';
import { useRoute} from 'vue-router';
import { defineComponent,} from 'vue';

export default defineComponent({
  name: 'Detail',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,IonButtons, IonBackButton
  },
  setup(){
    const route = useRoute();
    const { id } = route.params;

    return {id}
  }
});
</script>

<style scoped></style>
