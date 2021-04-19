<template>
  <div id="container">
    <div id="header">
      <Navbar />
    </div>
    <div id="body">
      <h1>Kontakt</h1>
      <div id="erstercontainer">
        <hr class="dashed" />
        <img src="~assets/pizza2.png" alt="Pizza vector" /><img />
        <hr class="dashed" />
      </div>
      <h2>
        Wir sind neugierig auf Ihr Feedback! Schreiben Sie uns gerne eine
        Nachricht.
      </h2>
      <div>
        <div class="container">
          <form action="action_page.php">
            <label for="vname">Vorname</label>
            <input
              type="text"
              id="vname"
              name="vorname"
              placeholder="Vorname"
            />

            <label for="nname">Nachname</label>
            <input
              type="text"
              id="nname"
              name="nachname"
              placeholder="Nachname"
            />

            <label for="ges">Geschlecht</label>
            <select id="ges" name="geschlecht">
              <option value="m">m</option>
              <option value="w">w</option>
              <option value="d">d</option>
            </select>

            <label for="nachricht">Nachricht:</label>
            <textarea
              id="nachricht"
              name="nachricht"
              placeholder="Nachricht eingeben."
              style="height: 200px"
            ></textarea>

            <input type="submit" value="Senden" />
          </form>
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

#footer {
  display: flex;
  width: 100vw;
  background-color: rgb(250, 241, 228);
  font-family: "Bitter", serif;
  justify-content: center;
  align-items: center;
}

#body::-webkit-scrollbar {
  display: none;
}

h1 {
  text-align: center;
  font-family: "Bitter", serif;
  font-size: 8vh;
}

h2 {
  font-family: "Bitter", serif;
  font-size: 3vh;
  margin-top: 3vh;
  margin-bottom: 5vh;
}

hr.dashed {
  display: flex;
  width: 100%;
  border-top: 3px dashed #bbb;
  align-self: center;
}

#erstercontainer {
  display: flex;
  width: 90vw;
  justify-content: center;
}

input[type="text"],
select,
textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
}

input[type="submit"] {
  background-color: gray;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type="submit"]:hover {
  background-color: darkred;
}

.container {
  border-radius: 5px;
  background-color: #f2f2f2;
  padding: 20px;
  margin-bottom: 5vh;
}
</style>