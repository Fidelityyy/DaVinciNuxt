<template>
  <div id="container">
    <div id="header">
      <Navbar />
    </div>
    <div id="body">
      <h1 id="überschrift">Historie</h1>
      <div id="erstercontainer">
        <hr class="dashed" />
        <img src="~assets/pizza2.png" alt="Pizza vector" /><img />
        <hr class="dashed" />
      </div>
      <div id="leonardocontainer">
        <div id="leonardobox">
          <img src="~assets/davinciportait.jpg" id="leonardobild" />
          <p id="#leonardobildunterschrift">Leonardo Da Vinci</p>
        </div>
        <p id="leonardotext">
          Die Geschichte unseres Unternehmens fängt im Jahre 1472 an, als der
          Gründer unserer Pizzeria, Leonardo Da Vinci, sich mit 20 Jahren dazu
          entschließt, sein Hobby zum Beruf zu machen und eine Pizzeria zu
          gründen.<br />Da Vinci - eher bekannt durch seine literarischen Werke
          - ist selbst ein großer Pizza-Fan mit Leib und Seele. Er versucht die
          Branche mit seinen ausgefallenen Kreationen zu revolutionieren und
          scheut dabei keinerlei Kosten und Mühe.
        </p>
      </div>
      <div id="ofenpizzabox">
        <p id="ofentext">
          Diese Einstellung von Da Vinci haben wir uns zum Motto gemacht! Wir
          bieten Ihnen stets neue Kreationen zu unschlagbarem Preis. <br />
          Hierfür verwenden wir natürliche stets frische und echt italienische
          Zutaten.
        </p>
        <img src="~assets/ofenpizza.jpg" id="ofenpizza" />
      </div>
      <div id="pizzeria">
        <img src="~assets/pizzeria.webp" id="pizzeriabild" /><img />
        <p id="pizzeriatext">
          Unser Ristorante bietet Ihnen ein Ambiente, das seinesgleichen sucht.
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
    <div id="footer">
      <p>
        Max Mustermann - Mustermannstraße 23 - 35234 Musterstadt - Steuernummer:
        00000000000 - Landgericht Musterstadt
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
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

#erstercontainer {
  display: flex;
  width: 100vw;
  justify-content: center;
}

hr.dashed {
  display: flex;
  width: 40%;
  border-top: 3px dashed #bbb;
  align-self: center;
}

#leonardotext {
  display: flex;
  align-items: center;
  text-align: center;
  margin-right: 10vw;
  margin-left: 10vw;
  font-family: "Bitter", serif;
  background-color: floralwhite;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
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
  margin-top: 5vh;
}

#ofenpizzabox {
  display: flex;
  flex-direction: row;
  align-items: center;
}

#ofenpizza {
  border-radius: 5%;
  width: 20vw;
  height: auto;
  margin-right: 10vw;
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
  background-color: bisque;
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
  display:flex;
  flex-direction: column;
}

#überschrift {
  text-align: center;
  font-family: "Bitter", serif;
  font-size: 8vh;
}

#footer {
  display: flex;
  width: 100vw;
  background-color: antiquewhite;
  font-family: "Bitter", serif;
  justify-content: center;
  align-items: center;
}
</style>