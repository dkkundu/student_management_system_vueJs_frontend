<template>

<nav class="navbar navbar-expand-lg navbar-dark bg-color">
  <div class="container-fluid">
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Student</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Management
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
          </ul>
        </li>
         <li class="nav-item">
          <a class="nav-link" href="#">Registation</a>
        </li>
      </ul>
      <form class="d-flex">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </div>
</nav>







</template>

<script>
    export default {
         name: 'NavBar',
        
    }
</script>

<style scoped>
.btn-outline-success {
    color: #000;
    background-color: #fff;
    border-color: #fdfdfd;
}
.btn-outline-success :hover{
    color: #000;
    background-color: rgb(50, 233, 74);
    border-color: #16e484;
}
.nav-link {
    color: #fdfdfd !important;
    font-weight: 511 !important;
}
.bg-color {
    background-color: #0d98ae !important;
}
.body {
    background-color: #699e611c I !important;
}


</style>