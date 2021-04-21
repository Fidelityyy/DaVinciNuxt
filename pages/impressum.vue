<template>
  <div class="container">
    <div class="header">
      <Navbar />
    </div>
    <div class="body">
      <h1 class="bodyüberschrift">Impressum</h1>
      <PizzaTrenner />
      <div class="impressumstext">
        <p1 class="text">
          <b>Name:</b> Da Vinci, Leonardo<br /><b>Adresse:</b> Davincistraße 23
          in Anchiano, Italien<br /><b>Kontakt:</b> Telefonnummer: +3912345678,
          E-Mail: leonardo@davinci.it<br><b>Handelsregisternr.:</b> 0001242342
        </p1>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
export default {};
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

.impressumstext {
  margin-left: 10vw;
  margin-right: 10vw;
  text-align: justify;
}
</style>