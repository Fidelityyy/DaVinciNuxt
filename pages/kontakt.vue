<template>
  <Div id="container">
    <Div id="header">
      <Navbar />
    </Div>
    <Div id="body">
      <H1>Kontakt</H1>
      <Div id="erstercontainer">
        <Hr class="dashed" />
        <Img src="~assets/pizza2.png" alt="Pizza vector" /><Img />
        <Hr class="dashed" />
      </Div>
      <H2>
        Wir sind neugierig auf Ihr Feedback! Schreiben Sie uns gerne eine
        Nachricht.
      </H2>
      <Div>
        <Div class="container">
          <Form action="action_page.php">
            <Label for="vname">Vorname</Label>
            <Input
              type="text"
              id="vname"
              name="vorname"
              placeholder="Vorname"
            />

            <Label for="nname">Nachname</Label>
            <Input
              type="text"
              id="nname"
              name="nachname"
              placeholder="Nachname"
            />

            <Label for="ges">Geschlecht</Label>
            <Select id="ges" name="geschlecht">
              <Option value="m">m</Option>
              <Option value="w">w</Option>
              <Option value="d">d</Option>
            </Select>

            <Label for="nachricht">Nachricht:</Label>
            <TextArea
              id="nachricht"
              name="nachricht"
              placeholder="Nachricht eingeben."
              style="height: 200px"
            ></TextArea>

            <Label class="container">
              <Input type="checkbox" />
              <Span class="checkmark"></Span>
              Ich bin mit den Datenschutzbestimmungen einverstanden.
            </Label>

            <Input type="submit" value="Senden" />
          </Form>
        </Div>
      </Div>
    </Div>
    <Footer />
  </Div>
</template>

<script>
export default {
  name: "kontakt",
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