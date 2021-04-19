<template>
  <div id="container">
    <div id="header">
      <Navbar></Navbar>
    </div>
    <div id="body"></div>
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
  grid-template-rows: 12.5vh 12.5vh 12.5vh 12.5vh 12.5vh 12.5vh 12.5vh 12.5vh;
  grid-template-areas:
    "header header header header header"
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
  justify-content: center;
  align-self: center;
}

#footer {
  background-color: aqua;
  width: 100vw;
}
</style>