<template>
  <b-navbar toggleable="lg" type="light" id="navigation">
    <b-navbar-brand id ="logo" href="/">DaVinci</b-navbar-brand>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item href="#">Historie</b-nav-item>
        <b-nav-item href="#">Kontakt</b-nav-item>
      </b-navbar-nav>
      <b-navbar-nav class="ml-auto">
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {};
</script>

<style>
#navigation {
  height: 100%;
  background-color:rgb(250, 241, 228);
}

#logo {
    font-family: 'Great Vibes', cursive;
    font-size: 5vh;
    color:black;
}

#logo:hover {
      font-family: 'Great Vibes', cursive;
    font-size: 5vh;
    color:darkred;
}
</style>