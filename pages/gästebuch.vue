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
        <!--         <div class="loginarea">
          <p>Login:</p>

          <input
            v-model.lazy="benutzername"
            placeholder="Benutzername"
            class="benutzernamefeld"
          />
          <input
            v-model.lazy="passwort"
            placeholder="Passwort"
            class="passwortfeld"
          />
        </div> -->
        <button @click="elementEinfügen()" class="sendenknopf">Senden</button>
      </div>
      <div v-for="eingabe in eingaben" v-bind:key="eingabe.nachricht">
        <GaestebuchEintrag
          v-bind:elementname="eingabe.name"
          :elementnachricht="eingabe.nachricht"
          :index="eingabe.index"
          @geloescht="elementLoeschen"
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
      index: 0,
      eingaben: [],
    };
  },
  methods: {
    elementEinfügen() {
      let name = this.name;
      let nachricht = this.nachricht;
      let index;
      einfuegaktion: for (let i = 0; i < this.eingaben.length; i++) {
        if (typeof this.eingaben[i] == "undefined") {
          this.index = i;
          break einfuegaktion;
        }
      }
      restfunktion: 
      index = this.index;
      this.eingaben.push({ name, nachricht, index });
      this.index++;
      this.name = "";
      this.nachricht = "";
    },
    elementLoeschen(index) {
      this.eingaben.splice(index, 1);
      this.index = this.eingaben.length;
      for(let i = 0; i < this.eingaben.length; i++) {
        this.eingaben[i].index = i;
      }
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
  border-radius: 3%;
  padding-bottom: 5vh;
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

.loginarea {
  margin-top: 2vh;
  margin-left: 2vw;
  display: flex;
  flex-direction: column;
  width: 50%;
}

.logintickbox {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.benutzernamefeld {
  margin-bottom: 1vh;
}

.passwortfeld {
  margin-top: 1vh;
}

.sendenknopf {
  align-self: center;
  width: 10vw;
  margin-top: 5vh;
  box-shadow: inset 0px 1px 0px 0px #ffffff;
  background: linear-gradient(to bottom, #f9f9f9 5%, #e9e9e9 100%);
  background-color: #f9f9f9;
  border-radius: 6px;
  border: 1px solid #dcdcdc;
  display: inline-block;
  cursor: pointer;
  color: #666666;
  font-family: Arial;
  font-size: 15px;
  font-weight: bold;
  padding: 6px 24px;
  text-decoration: none;
  text-shadow: 0px 1px 0px #ffffff;
  margin-right: 1vw;
}

.sendenknopf:hover {
  background: linear-gradient(to bottom, #e9e9e9 5%, #f9f9f9 100%);
  background-color: #e9e9e9;
}
.sendenknopf:active {
  position: relative;
  top: 1px;
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