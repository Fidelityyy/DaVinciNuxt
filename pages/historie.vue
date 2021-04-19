<template>
  <Div id="container">
    <Div id="header">
      <Navbar />
    </Div>
    <Div id="body">
      <H1 id="überschrift">Historie</H1>
      <Div id="erstercontainer">
        <Hr class="dashed" />
        <img src="~assets/pizza2.png" alt="Pizza vector" />
        <Hr class="dashed" />
      </Div>
      <Div id="leonardocontainer">
        <Div id="leonardobox">
          <img src="~assets/davinciportait.jpg" id="leonardobild" />
          <P id="#leonardobildunterschrift">Leonardo Da Vinci</P>
        </Div>
        <P id="leonardotext">
          Die Geschichte unseres Unternehmens fängt im Jahre 1472 an, als der
          Gründer unserer Pizzeria, Leonardo Da Vinci, sich mit 20 Jahren dazu
          entschließt, sein Hobby zum Beruf zu machen und eine Pizzeria zu
          gründen.<Br />Da Vinci - eher bekannt durch seine künstlerischen Werke
          und Erfindungen - ist selbst ein großer Pizza-Fan mit Leib und Seele.
          1940 nimmt er, nach seiner 4 jährigen kulinarischen Weltreise, an den
          internationalen Pizzaweltmeisterschaften Teil und gewinnt den dritten
          Platz mit seiner "Chilly-Schokoladen-Pizza". Aus der Frustration und
          seines Ehrgeizes heraus, zu der Spitze zu gehören, erfindet er die
          noch heute international äußerst beliebte "8 -Käse-Pizza". Mit dieser
          Weltneuheit gelingt es ihm nicht nur den ersten Platz in der Kategorie
          "Beste Pizza" sondern auch den ersten Platz in der Kategorie "Größter Käseanteil" für
          sich zu beanspruchen. Bis heute versucht er die Branche mit seinen ausgefallenen
          Kreationen zu revolutionieren und scheut dabei keinerlei Kosten und
          Mühe.
        </P>
      </Div>
      <Div id="ofenpizzabox">
        <P id="ofentext">
          Diese Einstellung von Da Vinci haben wir uns zum Motto gemacht! Wir
          bieten Ihnen stets neue Kreationen zu unschlagbarem Preis. <Br />
          Hierfür verwenden wir natürliche stets frische und echt italienische
          Zutaten.
        </P>
        <img src="~assets/ofenpizza.jpg" id="ofenpizza" />
      </Div>
      <Div id="pizzeria">
        <img src="~assets/pizzeria.webp" id="pizzeriabild" />
        <P id="pizzeriatext">
          Unser Ristorante bietet Ihnen ein Ambiente, das seinesgleichen sucht.
          Genießen Sie eine leckere Margherita-Pizza, während Sie den Abend auf
          unserer Terasse mit Meeresblick ausklingen lassen oder entspannen Sie
          sich an unserem Kamin zu einem köstlichen Cappucino.
        </P>
      </Div>
      <Div id="zahlungsmethoden">
        <img src="~assets/kreditkarte.png" id="kreditkarte" />
        <Div id="zahlungstextbox">
          <H1 id="zahlungsüberschrift">
            Haben Sie mal nicht das nötige Geld dabei? Kein Problem!
          </H1>
          <P1 id="zahlungsmethodentext"
            >Bei uns können Sie in Bar oder bequem per Debitkarte bezahlen -
            natürlich kontaktlos!</P1
          >
        </Div>
      </Div>
    </Div>
    <Footer />
  </Div>
</template>

<script>
export default {
  name: "historie",
};
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