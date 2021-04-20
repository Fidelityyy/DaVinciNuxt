<template>
  <div class="container">
    <div class="header">
      <Navbar />
    </div>
    <div class="body">
      <h1 class="bodyüberschrift">Gästebuch</h1>
      <PizzaTrenner />
      <div class="formular">
        <input v-model.lazy="name" placeholder="Name" class="namensfeld" />
        <textarea
          v-model.lazy="nachricht"
          placeholder="Nachricht"
          class="nachrichtfeld"
        />
        <button @click="elementEinfügen()" class="sendenknopf">Senden</button>
      </div>
      <div v-for="eingabe in eingaben" v-bind:key="eingabe.nachricht">
        <GaestebuchEintrag
          v-bind:elementname="eingabe.name"
          :elementnachricht="eingabe.nachricht"
        />
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import PizzaTrenner from "../components/PizzaTrenner.vue";
export default {
  components: { PizzaTrenner },
  name: "gästebuch",
  data() {
    return {
      name: "",
      nachricht: "",
      eingaben: [],
    };
  },
  methods: {
    elementEinfügen() {
      let name = this.name;
      let nachricht = this.nachricht;
      this.eingaben.push({ name, nachricht });
      this.name = "";
      this.nachricht = "";
    },
    elementLöschen() {
    },
  },
};
</script>

<style scoped>
.container {
  display: grid;
  width: 100vw;
  height: 100vh;
  margin: 0;
  padding: 0;
  grid-template-columns: 20vw 20vw 20vw 20vw 20vw;
  grid-template-rows: 10vh 10vh 10vh 10vh 10vh 10vh 10vh 10vh 10vh 10vh;
  grid-template-areas:
    "header header header header header"
    "body body body body body"
    "body body body body body"
    "body body body body body"
    "body body body body body"
    "body body body body body"
    "body body body body body"
    "body body body body body"
    "body body body body body"
    "footer footer footer footer footer";
}

.header {
  grid-area: header;
}

.body {
  display: flex;
  grid-area: body;
  padding-top: 10vh;
  flex-direction: column;
  overflow-y: auto;
  -ms-overflow-style: none;
  scrollbar-width: none;
  width: 100vw;
}

.bodyüberschrift {
  text-align: center;
  font-family: "Bitter", serif;
  font-size: 8vh;
}

.formular {
  display: flex;
  justify-content: center;
  flex-direction: column;
  background-color: floralwhite;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  margin-left: 30vw;
  margin-right: 30vw;
  padding-bottom: 2vh;
  padding-top: 2vh;
  border-radius: 3%;
  margin-bottom: 5vh;
}

.namensfeld {
  margin-top: 5vh;
  margin-bottom: 5vh;
  width: 10vw;
  align-self: flex-start;
  margin-left: 2vw;
}

.nachrichtfeld {
  width: 30vw;
  margin-left: 2vw;
}

.sendenknopf {
  align-self: center;
  width: 10vw;
  margin-top: 5vh;
}

.einträge {
  display: flex;
  background-color: floralwhite;
  margin-top: 10vh;
  margin-left: 10vw;
  margin-right: 10vw;
  flex-direction: column;
  border-radius: 2%;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
</style>