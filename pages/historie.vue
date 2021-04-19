<template>
  <div id="container">
    <div id="header">
      <Navbar />
    </div>
    <div id="body">
      <h1>Historie</h1>
      <div id="erstercontainer">
        <hr class="dashed" />
        <img src="~assets/pizza2.png" alt="Pizza vector" /><img />
        <hr class="dashed" />
      </div>
      <div id = "leonardocontainer">
      <div id="leonardobox">
        <img src="~assets/davinciportait.jpg" id = "leonardobild"/>
        <p id="#leonardobildunterschrift">Leonardo Da Vinci</p>
      </div>
          <p id="leonardotext">
          Die Geschichte unserer Pizzeria fängt im Jahre 1472 an, als der
          Gründer unserer Pizzeria, Leonardo Da Vinci, sich mit 20 Jahren dazu
          entschließt, sein Hobby zum Beruf zu machen und eine Pizzeria zu
          gründen.
        </p>
      </div>
    </div>
    <div id="footer"><p>Max Mustermann - Mustermannstraße 23 - 35234 Musterstadt - Steuernummer: 00000000000 - Landgericht Musterstadt</p></div>
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
  text-align: center;
  margin-right: 10vw;
  margin-left: 10vw;
  font-family: "Bitter", serif;
  background-color: floralwhite;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19)
}

#leonardobox {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin-left: 10vw;
}

#leonardocontainer {
  display:flex;
  margin-top: 5vh;
}

#leonardobild {
  border-radius: 50%;
  width: 10vw;
  margin-bottom: 1vh;
  height: auto;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.7), 0 6px 20px 0 rgba(0, 0, 0, 0.19)
}

#leonardobildunterschrift {
  font-family: "Great Vibes", cursive;
}

#footer {
  display:flex;
  width: 100vw;
  background-color: antiquewhite;
  font-family: "Bitter", serif;
  justify-content: center;
  align-items: center;
}

h1 {
  text-align: center;
  font-family: "Bitter", serif;
  font-size: 8vh;
}
</style>