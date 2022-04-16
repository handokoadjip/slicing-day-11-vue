<template>
  <header class="min-vh-100 position-relative">
    <nav class="navbar fixed-top navbar-light px-4">
      <div class="container-fluid px-0 d-flex justify-content-between">
        <div class="d-flex justify-content-center align-items-center">
          <router-link class="text-decoration-none me-4 circle-icon" to="#"><i class="fab fa-facebook-f"></i>
          </router-link>
          <router-link class="text-decoration-none circle-icon" to="#"><i class="fab fa-twitter"></i></router-link>
        </div>
        <router-link class="navbar-brand text-center d-none d-lg-block text-uppercase mp-0 fw-bolder" to="#">
          mitravel
        </router-link>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav text-uppercase">
            <li class="nav-item px-0 px-lg-4">
              <router-link class="nav-link text-center" aria-current="page" to="#">work</router-link>
            </li>
            <li class="nav-item px-0 px-lg-4">
              <router-link class="nav-link text-center" to="#">home</router-link>
            </li>
            <li class="nav-item px-0 px-lg-4">
              <router-link class="nav-link text-center" to="#">about</router-link>
            </li>
            <li class="nav-item px-0 px-lg-4">
              <router-link class="nav-link text-center" to="#">contact</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <section>
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="wrapper text-center">
              <div class="position-absolute top-50 start-50 translate-middle">
                <h1 class="display-1 px-5 fw-bolder">Inspirations</h1>
                <small class="fs-5 text-fade-black-1">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Consequuntur vel harum quasi dolor, molestias amet?</small>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
}
</script>

