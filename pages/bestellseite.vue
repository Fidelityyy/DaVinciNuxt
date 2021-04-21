<template>
  <div class="container">
    <div class="header">
      <Navbar />
    </div>
    <div class="body">
      <h1 class="bodyüberschrift">Bestellen</h1>
      <PizzaTrenner />
      <div class="bestellcontainer">
        <div class="bestellbox">
          <div class="gericht" style="border: none">
            <a
              href="#"
              @click="
                name = 'Pizza Margherita';
                preis = 16.99;
                elementEinfügen();
              "
              class="gericht"
              >Pizza Margherita - <b>16.99€</b></a
            >
            <a
              href="#"
              @click="
                name = 'Pizza Schinken';
                preis = 18.99;
                elementEinfügen();
              "
              class="gericht"
              >Pizza Schinken - <b>18.99€</b></a
            >
            <a
              href="#"
              @click="
                name = 'Pizza Salami';
                preis = 18.99;
                elementEinfügen();
              "
              class="gericht"
              >Pizza Salami - <b>18.99€</b></a
            >
            <a
              href="#"
              @click="
                name = 'Pizza Tonno';
                preis = 17.99;
                elementEinfügen();
              "
              class="gericht"
              >Pizza Tonno - <b>17.99€</b></a
            >
            <a
              href="#"
              @click="
                name = 'Pizza Hawaii';
                preis = 20.99;
                elementEinfügen();
              "
              class="gericht"
              >Pizza Hawaii - <b>20.99€</b></a
            >
            <a
              href="#"
              @click="
                name = 'Pizza 4 Kaese';
                preis = 22.99;
                elementEinfügen();
              "
              class="gericht"
              >Pizza 4 Käse - <b>22.99€</b></a
            >
          </div>
          <div class="menubestellt">
            <p>Bestellung:</p>
            <div
              v-for="gericht in gerichte"
              v-bind:key="gericht.index"
              class="gerichtsblock"
            >
              <Gericht
                v-bind:elementname="gericht.name"
                :elementpreis="gericht.preis"
                :index="gericht.index"
              />
            </div>
            <div class="preisblock">
              <p>Preis: {{ gesamtpreisberechnet }}€</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  name: "bestellseite",
  data() {
    return {
      index: 0,
      name: "",
      preis: 0.00,
      gerichte: [],
      gesamtpreis: 0.00,
    };
  },
  methods: {
    elementEinfügen() {
      let name = this.name;
      let preis = this.preis;
      let index;
      einfuegaktion: for (let i = 0; i < this.gerichte.length; i++) {
        if (typeof this.gerichte[i] == "undefined") {
          this.index = i;
          break einfuegaktion;
        }
      }
      restfunktion: index = this.index;
      this.gerichte.push({ name, preis, index });
      this.index++;
      this.name = "";
      this.preis = "";
    },
  },
  computed: {
      gesamtpreisberechnet: function() {
          for(let gericht in this.gerichte) {
              this.gesamtpreis += gericht.elementpreis;
          }
          return this.gesamtpreis;
      }

  }
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

.bestellbox {
  margin-left: 20vw;
  margin-right: 20vw;
  display: flex;
}

.menubestellt {
  border: 1px solid #000000;
  font-family: "Bitter", serif;
  font-size: 5vh;
  padding-left: 2vw;
  padding-right: 2vw;
  display: flex;
  flex-direction: column;
  width: 40vw;
  margin-bottom: 10vh;
  align-self: center;
  height: 70vh;
  overflow-y: auto;
  -ms-overflow-style: none;
  scrollbar-width: none;
}

.gericht {
  align-items: center;
  justify-content: center;
  width: 100%;
  display: flex;
  background-color: #ffffff;
  border: 1px solid #000000;
  display: inline-block;
  cursor: pointer;
  color: #000000;
  font-family: "Bitter", serif;
  font-size: 28px;
  padding: 19px 76px;
  text-decoration: none;
  text-shadow: 0px 1px 50px #adadad;
  margin-bottom: 1vw;
}
.gericht:hover {
  background-color: #ffffff;
}
.gericht:active {
  position: relative;
  top: 1px;
}
</style>