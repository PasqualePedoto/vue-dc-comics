<!-- # Descrizione:
Create un nuovo progetto utilizzando Vue CLI e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass!

# Bonus:
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.
Questo bonus nasconde un'insidia legata alla renderizzazione delle immagini che potrebbe 
farvi venire qualche grattacapo! Cercate di trovare una soluzione da veri programmatori e 
proprio in caso di emergenza, aprite un ticket! -->

<template>
  <div class="set-display">
    <TheHeader />
    <TheMain />
    <TheFooter />
    <TheBottomFooter />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import TheMain from "./components/TheMain.vue";
import TheFooter from "./components/TheFooter.vue";
import TheBottomFooter from "./components/TheBottomFooter.vue";

export default {
  name: "DC-Comics",
  components: {
    TheHeader,
    TheMain,
    TheFooter,
    TheBottomFooter,
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss">
// GENERICS

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

img {
  max-width: 100%;
  height: 100%;
}

a {
  text-decoration: none;
}

ul > li {
  list-style-type: none;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  height: auto;
}

.set-display {
  display: flex;
  flex-direction: column;

  position: relative;
}
</style>
