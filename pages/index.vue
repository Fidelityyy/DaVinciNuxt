<template>
  <div id="container">
    <div id="header">
      <Navbar />
    </div>
    <div id="body">
      <div id="logoarea">
        <h1 id="logomain"><span style="color: DarkRed">Da</span>Vinci</h1>
        <p id="untertitel">Die Pizzeria Ihres Vertrauens!</p>
      </div>
      <hr class="dashed" />
      <div id="inhalt">
        <div id="pizzavector">
          <img
            src="~assets/pizza.png"
            alt="Pizza vector"
            style="width: 20vw; height: auto; margin-top: 5vh"
          />
        </div>
      </div>
    </div>
    <Footer/>
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
export default {
  name: "index",
  components: { Navbar },
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
  width: 100vw;
  background-image: url("~assets/davinci2.jpg");
  background-size: 80%;
  background-position: top;
}

#logomain {
  font-family: "Great Vibes", cursive;
  font-size: 20vh;
  text-align: center;
}

#untertitel {
  text-align: center;
  font-family: "Bitter", serif;
  font-size: 4vh;
}

hr.dashed {
  display: flex;
  border-top: 3px dashed #bbb;
  width: 80vw;
  align-self: center;
}

#pizzavector {
  display: flex;
  justify-content: center;
}

#body::-webkit-scrollbar {
  display: none;
}
</style>