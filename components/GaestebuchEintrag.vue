<template>
  <div class="nachrichten">
    <p class="angezeigterindex"><b>Index</b>: {{ index }}</p>
    <p class="angezeigtername"><b>Name</b>: {{ elementname }}</p>
    <p class="angezeigtenachricht"><b>Nachricht</b>: {{ elementnachricht }}</p>
    <div class="interaktionsknöpfe">
      <button class="bearbeitenknopf">Bearbeiten</button>
      <button @click="emitten" class="löschenknopf">
        Löschen
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "gaestebuch",
  props: ["elementname", "elementnachricht", "index"],
  methods: {
    emitten() {
      this.$emit('geloescht', this.index)
    },
  },
};
</script>

<style scoped>
.nachrichten {
  display: flex;
  flex-direction: column;
  display: flex;
  justify-content: center;
  flex-direction: column;
  background-color: floralwhite;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  margin-left: 20vw;
  margin-right: 20vw;
  margin-bottom: 5vh;
  padding-bottom: 2vh;
  padding-top: 2vh;
  border-radius: 3%;
}

.angezeigtername {
  margin-left: 5vw;
}

.angezeigterindex {
  margin-top: 5vh;
  margin-left: 5vw;
}

.angezeigtenachricht {
  margin-left: 5vw;
  margin-bottom: 5vh;
}

.interaktionsknöpfe {
  display: flex;
  justify-content: center;
}

.bearbeitenknopf {
  box-shadow: inset 0px 1px 0px 0px #ffffff;
  background: linear-gradient(to bottom, #f9f9f9 5%, #e9e9e9 100%);
  background-color: #f9f9f9;
  border-radius: 6px;
  border: 1px solid #dcdcdc;
  display: inline-block;
  cursor: pointer;
  color: #666666;
  font-family: Arial;
  font-size: 15px;
  font-weight: bold;
  padding: 6px 24px;
  text-decoration: none;
  text-shadow: 0px 1px 0px #ffffff;
  margin-right: 1vw;
}

.löschenknopf {
  box-shadow: inset 0px 1px 0px 0px #ffffff;
  background: linear-gradient(to bottom, #f9f9f9 5%, #e9e9e9 100%);
  background-color: #f9f9f9;
  border-radius: 6px;
  border: 1px solid #dcdcdc;
  display: inline-block;
  cursor: pointer;
  color: #666666;
  font-family: Arial;
  font-size: 15px;
  font-weight: bold;
  padding: 6px 24px;
  text-decoration: none;
  text-shadow: 0px 1px 0px #ffffff;
  margin-left: 1vw;
}

.löschenknopf:hover {
  background: linear-gradient(to bottom, #e9e9e9 5%, #f9f9f9 100%);
  background-color: #e9e9e9;
}
.löschenknopf:active {
  position: relative;
  top: 1px;
}

.bearbeitenknopf:hover {
  background: linear-gradient(to bottom, #e9e9e9 5%, #f9f9f9 100%);
  background-color: #e9e9e9;
}
.bearbeitenknopf:active {
  position: relative;
  top: 1px;
}
</style>