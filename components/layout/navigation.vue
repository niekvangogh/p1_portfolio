<template>
  <b-nav class="navbar-toggleable-sm navbar-trans navbar-inverse">
    <b-container>
      <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse"
              data-target="#navbarToggler-1" aria-controls="navbarToggler-1" aria-expanded="false"
              aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <a class="navbar-brand" href="#">Bootstrap 4 Cover Nav</a>
      <div class="collapse navbar-collapse pull-xs-right justify-content-end" id="navbarToggler-1">
        <ul class="navbar-nav mt-2 mt-md-0">
          <li class="nav-item active">
            <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Our Work</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Contact</a>
          </li>
          <li class="nav-item">
            <a class="btn btn-outline-white btn-outline" href="#"><i class="fa fa-user"></i> Login
            </a>
          </li>
        </ul>
      </div>
    </b-container>
  </b-nav>
</template>
<script>
  export default {
    name: "navigation"
  }
</script>
<style lang="scss">

</style>
