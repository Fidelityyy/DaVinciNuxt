<template>
  <div id="erstercontainer">
    <hr class="dashed" />
    <img src="~assets/pizza2.png" alt="Pizza vector" /><img />
    <hr class="dashed" />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
#erstercontainer {
  display: flex;
  width: 80vw;
  justify-content: center;
  align-self: center;
  margin-bottom: 5vh;
}

hr.dashed {
  display: flex;
  width: 100%;
  border-top: 3px dashed #bbb;
  align-self: center;
}
</style>