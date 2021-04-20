<template>
  <div class="nachrichten">
    <p1 class="angezeigtername">Name: {{ elementname }}</p1>
    <p1 class="angezeigtenachricht">Nachricht : {{ elementnachricht }}</p1>
  </div>
</template>

<script>
export default {
  name: "gaestebuch",
  props: ["elementname", "elementnachricht", "index"],
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
  margin-left: 10vw;
  margin-right: 10vw;
  margin-bottom: 5vh;
  padding-bottom: 2vh;
  padding-top: 2vh;
  border-radius: 3%;
}

.angezeigtername {
  margin-top: 10vh;
  margin-left: 5vw;
}

.angezeigtenachricht {
  margin-left: 5vw;
  margin-bottom: 10vh;
}
</style>