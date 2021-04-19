<template>
  <div id="container">
    <div id="header">
      <Navbar></Navbar>
    </div>
    <div id="body">
      <h1 id="logomain"><span style = "color: DarkRed">Da</span>Vinci</h1>
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
  background-image: url("https://upload.wikimedia.org/wikipedia/commons/f/f1/Vitruvian_Man_by_Leonardo_da_Vinci.jpg");
  background-repeat: repeat-y;
  background-size: 100%;
  background-color: antiquewhite;
}

#header {
  grid-area: header;
}

#body {
  display: flex;
  grid-area: body;
  justify-content: center;
  align-self: center;
}

#logomain {
  font-family: "Great Vibes", cursive;
  font-size: 20vh;
}

#footer {
  background-color: aqua;
  width: 100vw;
  background-color: antiquewhite;
}
</style>