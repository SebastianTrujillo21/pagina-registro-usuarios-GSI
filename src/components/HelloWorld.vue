<template>
  <div>
    <v-container class="contenedor">
      <v-row class="contenido">
        <v-col cols="12">
          <v-time-picker v-model="tiempo" disabled use-seconds></v-time-picker>
        </v-col>
        <v-col cols="12" class="mt-5">
          <div>
            <v-alert
              v-model="alert"
              border="left"
              close-text="Close Alert"
              color="blue accent-4"
              dark
              dismissible
            >
              Se ha marcado correctamente la asistencia de este usuario :D
            </v-alert>
            <div class="text-center">
              <button
                type="button"
                class="btn btn-primary boton"
                :disabled="isDisabled"
                v-if="!alert"
                v-on:click="marcarAsistencia"
              >
                Marca asistencia
              </button>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import { initializeApp } from "@firebase/app";
//import { getFirestore, collection } from "@firebase/firestore";

const firebaseConfig = {
  apiKey: "AIzaSyAtIqDVWo7oKBw94iw9sZEGYGySH66pFi8",
  authDomain: "gsi-vue-app.firebaseapp.com",
  databaseURL: "https://gsi-vue-app-default-rtdb.firebaseio.com",
  projectId: "gsi-vue-app",
  storageBucket: "gsi-vue-app.appspot.com",
  messagingSenderId: "901717682681",
  appId: "1:901717682681:web:0f93492298a318e96e7528",
  measurementId: "G-5GY7LC5C20",
};

const firebaseApp = initializeApp(firebaseConfig)
console.log(firebaseApp)


export default {
  name: "HelloWorld",
  data() {
    return {
      tiempo: new Date(),
      alert: false,
      isDisabled: false,
    };
  },
  methods: {
    marcarAsistencia() {
      this.alert = true;
      this.isDisabled = true;
    },
  },
};
</script>
<style>
.contenedor {
  margin: auto;
  padding: 90px;
  text-align: center;
}

.contenido {
  text-align: center;
  justify-content: center;
}
.boton {
  color: white;
}
</style>
