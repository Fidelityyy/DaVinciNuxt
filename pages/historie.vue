<template>
  <div id="container">
    <div id="header">
      <Navbar />
    </div>
    <div id="body">
      <h1 id="überschrift">Historie</h1>
      <PizzaTrenner />
      <div id="leonardocontainer">
        <div id="leonardobox">
          <img src="~assets/davinciportait.jpg" id="leonardobild" />
          <p id="#leonardobildunterschrift">Leonardo Da Vinci</p>
        </div>
        <p id="leonardotext">
          1472 - Eröffnung seiner ersten Pizzeria<br />1478 - Teilnahme an der
          internationalen Pizzaweltmeisterschaft<br />1482 - Promotion an der
          Hochschule für Ernährungswissenschaften in Wien<br />1490 - Eröffnung
          seiner Filiale in New York<br />
        </p>
      </div>
      <div id="ofenpizzabox">
        <p id="ofentext">
          1990 - Eröffnung unserer Filiale<br />1992 - Einführung unseres
          Lieferservices<br />1993 - Auszeichnung zur "Besten Pizzeria in der
          Region"<br />
          2005 - Eröffnung unserer Zweitfiliale in Hamburg
        </p>
        <img src="~assets/ofenpizza.jpg" id="ofenpizza" />
      </div>
      <div id="pizzeria">
        <img src="~assets/pizzeria.webp" id="pizzeriabild" />
        <p id="pizzeriatext">
          Unser Ristorante bietet Ihnen ein Ambiente, das seinesgleichen sucht.<br>
          Genießen Sie eine leckere Margherita-Pizza, während Sie den Abend auf
          unserer Terasse mit Meeresblick ausklingen lassen oder entspannen Sie
          sich an unserem Kamin zu einem köstlichen Cappucino.
        </p>
      </div>
      <div id="zahlungsmethoden">
        <img src="~assets/kreditkarte.png" id="kreditkarte" />
        <div id="zahlungstextbox">
          <h1 id="zahlungsüberschrift">
            Haben Sie mal nicht das nötige Geld dabei? Kein Problem!
          </h1>
          <p1 id="zahlungsmethodentext"
            >Bei uns können Sie in Bar oder bequem per Debitkarte bezahlen -
            natürlich kontaktlos!</p1
          >
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  name: "historie",
};
</script>

<style scoped>
#container {
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

#header {
  grid-area: header;
}

#body {
  display: flex;
  grid-area: body;
  justify-self: center;
  padding-top: 10vh;
  flex-direction: column;
  overflow-y: auto;
  -ms-overflow-style: none;
  scrollbar-width: none;
}

#body::-webkit-scrollbar {
  display: none;
}

#leonardotext {
  display: flex;
  align-items: center;
  text-align: center;
  margin-right: 10vw;
  margin-left: 10vw;
  padding-left: 2vw;
  padding-right: 2vw;
  font-family: "Bitter", serif;
  background-color: floralwhite;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  margin-bottom: 5vh;
  padding: 2vw;
}

#ofentext {
  display: flex;
  align-items: center;
  text-align: center;
  margin-right: 10vw;
  margin-left: 10vw;
  font-family: "Bitter", serif;
  background-color: floralwhite;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  padding: 2vw;
}

#leonardobox {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin-left: 10vw;
}

#leonardocontainer {
  display: flex;
  justify-content: space-evenly;
}

#ofenpizzabox {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-evenly;
  margin-right: 10vw;
}

#ofenpizza {
  border-radius: 5%;
  width: 20vw;
  height: auto;
}

#leonardobild {
  border-radius: 50%;
  width: 10vw;
  margin-bottom: 1vh;
  height: auto;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.7), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

#leonardobildunterschrift {
  font-family: "Great Vibes", cursive;
}
#pizzeriatext {
  display: flex;
  align-items: center;
  text-align: center;
  margin-right: 10vw;
  margin-left: 10vw;
  font-family: "Bitter", serif;
  background-color: floralwhite;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  padding: 2vw;
  width: 40vw;
}

#pizzeriabild {
  border-radius: 5%;
  width: 20vw;
  height: auto;
  margin-left: 10vw;
}

#pizzeria {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

#zahlungsmethoden {
  display: flex;
  background-image: linear-gradient(
    rgb(250, 241, 228),
    white,
    rgb(250, 241, 228)
  );
  margin-top: 5vh;
  align-items: center;
}

#zahlungsüberschrift {
  font-family: "Bitter", serif;
  font-size: 4vh;
}

#zahlungsmethodentext {
  display: flex;
  justify-content: center;
}

#kreditkarte {
  width: 30vw;
  height: auto;
}

#zahlungstextbox {
  display: flex;
  flex-direction: column;
}

#überschrift {
  text-align: center;
  font-family: "Bitter", serif;
  font-size: 8vh;
}
</style>