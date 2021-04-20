<template>
  <div class="footer">
    <p>
      Max Mustermann - Mustermannstraße 23 - 35234 Musterstadt - Steuernummer:
      00000000000 - Landgericht Musterstadt
    </p>
  </div>
</template>

<script>
export default {
    name: "Footer"
};
</script>

<style scoped>
.footer {
  display: flex;
  width: 100vw;
  background-color: rgb(250, 241, 228);
  font-family: "Bitter", serif;
  justify-content: center;
  align-items: center;
}
</style>