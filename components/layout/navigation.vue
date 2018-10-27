<template>
  <b-navbar toggleable="md">
    <b-container>

      <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
      <b-navbar-brand to="/">Media portfolio</b-navbar-brand>
      <b-collapse is-nav id="nav_collapse">
        <b-navbar-nav>
          <b-nav-item to="/">Home</b-nav-item>
          <b-nav-item-dropdown>
            <template slot="button-content">
              Portfolio
            </template>
            <b-dropdown-item to="/week/1">Week 1</b-dropdown-item>
            <b-dropdown-item to="/week/2">Week 2</b-dropdown-item>
            <b-dropdown-item to="/week/3">Week 3</b-dropdown-item>
            <b-dropdown-item to="/week/4">Week 4</b-dropdown-item>
            <b-dropdown-item to="/week/5">Week 5</b-dropdown-item>
            <b-dropdown-item to="/week/6">Week 6</b-dropdown-item>
            <b-dropdown-item to="/week/7">Week 7</b-dropdown-item>
          </b-nav-item-dropdown>
          <b-nav-item to="/geleerd">Wat heb ik geleerd?</b-nav-item>
          <b-nav-item to="/verder">Hoe wil ik nu verder?</b-nav-item>
          <b-nav-item to="/betekenis">Wat betekend deze website voor MIJ?</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-container>
  </b-navbar>
</template>
<script>
  export default {}
</script>
<style lang="scss">
  nav.navbar {
    .container {
      background-color: rgba(245, 245, 245, .3);

      a {
        color: white !important;
      }

      .dropdown-menu {
        background-color: rgba(78, 78, 80, .7);

        .dropdown-item {
          &:hover, .active, &:focus {
            background-color: white;
            color: black !important;
          }
        }
        .active {
          color: black;
        }
      }
    }
  }
</style>
