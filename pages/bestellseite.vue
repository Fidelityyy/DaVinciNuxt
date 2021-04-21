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
            <a href="#" @click="elementEinfügen()" class="gericht"
              >Pizza Margherita - <b>16.99</b></a
            >
            <a href="#" class="gericht">Pizza Schinken - <b>18.99</b></a>
            <a href="#" class="gericht">Pizza Salami - <b>18.99</b></a>
            <a href="#" class="gericht">Pizza Tonno - <b>17.99</b></a>
            <a href="#" class="gericht">Pizza Hawaii - <b>20.99</b></a>
            <a href="#" class="gericht"
              >Pizza Quattro Formaggi - <b>22.99</b></a
            >
          </div>
          <div class="menubestellt">
            <p>Bestellung:</p>
            <div>
              <Gericht />
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
      preis: 0,
      gerichte: [],
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