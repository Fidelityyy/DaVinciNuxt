<template>
  <div id="container">
    <div id="header">
      <Navbar/>
    </div>
    <div id="body">
      <div id="logoarea">
        <h1 id="logomain"><span style="color: DarkRed">Da</span>Vinci</h1>
        <p id="untertitel">Ihre Pizzeria des Vertrauens!</p>
      </div>
      <hr class = "dashed"/>
      <div id = "inhalt">
        <div id = "pizzavector">
          <img src = "https://sogno-mio.de/wp-content/uploads/2021/03/pngwing.com_-150x150.png" alt="Pizza vector"><img>
        </div>
      </div>
    </div>
    <div id="footer"></div>
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
export default {
  components: { Navbar },
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

#logomain {
  font-family: "Great Vibes", cursive;
  font-size: 20vh;
}

#untertitel {
  text-align: center;
  font-family: "Bitter", serif;
  font-size: 4vh;
}

hr.dashed {
  border-top: 3px dashed #bbb;
}

#pizzavector {
  display:flex;
  justify-content: center;
}

#body::-webkit-scrollbar {
  display:none;
}

#footer {
  width: 100vw;
  background-color: antiquewhite;
}
</style>