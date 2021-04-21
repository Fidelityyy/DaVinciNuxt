<template>
  <div class="containergericht">
    <p class="angezeigtername">{{ elementname }} - {{ elementpreis }}€</p>
  </div>
</template>

<script>
export default {
  name: "gericht",
  props: ["elementname","elementpreis", "index"],
};
</script>

<style scroped>
.containergericht {
  display: flex;
  flex-direction: column;
  /* border: 1px solid #000000; */
  font-size: 1vw;
}
</style>