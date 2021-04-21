<template>
  <BNavbar toggleable="lg" type="light" id="navigation">
    <BNavbarBrand id="logo" href="/">DaVinci</BNavbarBrand>
    <BNavbarToggle target="nav-collapse"></BNavbarToggle>
    <BCollapse id="nav-collapse" is-nav>
      <BNavbarNav>
        <BNavItem href="/historie">Historie</BNavItem>
        <BNavItem href="/bestellseite">Bestellen</BNavItem>
        <BNavItem href="/gästebuch">Gästebuch</BNavItem>
        <BNavItem href="/kontakt">Kontakt</BNavItem>
        <BNavItem href="/datenschutzbestimmungen">Datenschutzbestimmungen</BNavItem>
        <BNavItem href="/impressum">Impressum</BNavItem>
      </BNavbarNav>
      <BNavbarNav class="ml-auto"> </BNavbarNav>
    </BCollapse>
  </BNavbar>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped>
#navigation {
  height: 100%;
  background-color: rgb(250, 241, 228);
}

#logo {
  font-family: "Great Vibes", cursive;
  font-size: 5vh;
  color: black;
}

#logo:hover {
  font-family: "Great Vibes", cursive;
  font-size: 5vh;
  color: darkred;
}
</style>