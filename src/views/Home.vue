<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Blank</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>

      <div id="container">
        <ion-list>
          <ion-radio-group :value="selected" @ionChange="radioChange">
            <ion-list-header>
              <ion-label>Name</ion-label>
            </ion-list-header>

            <ion-item>
              <ion-label>Biff</ion-label>
              <ion-radio slot="start" value="biff"></ion-radio>
            </ion-item>

            <ion-item>
              <ion-label>Griff</ion-label>
              <ion-radio slot="start" value="griff"></ion-radio>
            </ion-item>

            <ion-item>
              <ion-label>Buford</ion-label>
              <ion-radio slot="start" value="buford"></ion-radio>
            </ion-item>
          </ion-radio-group>
          <ion-item>{{ selected }}</ion-item>
        </ion-list>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {IonContent, IonHeader, IonPage, IonTitle, IonToolbar} from '@ionic/vue';
import {defineComponent} from 'vue';

export default defineComponent({
  name: 'Home',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar
  },
  data() {
    return {
      selected: 'biff'
    }
  },
  methods: {
    radioChange: function (value: any) {
      console.log('radio changed to:', value);
    }
  }
});
</script>

<style scoped>
#container {
  text-align: center;

  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;

  color: #8C8C8C;

  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>