<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <RouterLink
          to="/" 
          class="nav-link active" aria-current="page" href="#">
          Home
        </RouterLink>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Menu
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <b-nav-item active-class="active" class="nav-link" v-for="routes in links" 
            :key="routes.id" :to="routes.path" >
            {{ routes.name }} 
            </b-nav-item>  
            <li>
              <RouterLink 
              to="/Products"
              class="dropdown-item">
              Products
              </RouterLink>
            </li>
            <li>
              <RouterLink
              to="/About"
              class="dropdown-item">
              About
              </RouterLink>
            </li>

          </ul>
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