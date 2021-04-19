<template>
  <div id="container">
    <div id="header">
      <Navbar />
    </div>
    <div id="body">
      <div id="erstescontainer">
        <hr class="dashed" />
        <img
          src="https://sogno-mio.de/wp-content/uploads/2021/03/pngwing.com_-150x150.png"
          alt="Pizza vector"
        /><img />
        <hr class="dashed" />
      </div>
      <div id="zweitercontainer">
        <div id="davinciblock">
          <img
            id="davinci"
            src="https://www.planet-schule.de/mm/nie-wieder-keine-ahnung/malerei/img/kuenstler_da_vinci.jpg"
            style="width: 10vw; height: auto; border-radius: 50%"
          /><img />
          <p>Leonardo Da Vinci</p>
        </div>
        <div id="pizzablock">
          <img
            id="pizzabild"
            src="https://www.koch-mit.de/app/uploads/2020/02/ofenpizza.jpg"
            style="width: 20vw; border-radius: 5%"
          /><img />
          <p>Unsere Pizzeria </p>
        </div>
      </div>
    </div>
    <div id="footer"></div>
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
  flex-direction: row;
  width: 100vw;
}

#zweitercontainer {
  display: flex;
  flex-direction: column;
  width: 100%;
  text-align: center;
}

#davinciblock {
  display:flex;
  flex-direction: column;
  align-self: start;
}

#pizzablock {
display:flex;
}

hr.dashed {
  border-top: 3px dashed #bbb;
}

#footer {
  grid-area: footer;
  width: 100vw;
  background-color: antiquewhite;
  height: 100%;
}
</style>