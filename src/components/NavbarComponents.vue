<template>
    <div>

      <!-- head header -->
        <div class="topNavBar py-2">
          <div class="container d-flex justify-content-center align-items-center">
              <div class="text-white">{{ company.name }}: ({{ company.contact }})</div>
              <div class="mx-md-5">
                  <a href="" class="btn appointment">Book an appointment</a>
              </div>
          </div>
        </div>

        <nav class="navbar navbar-expand-lg bg-light">
  <div class="container">
    <a class="navbar-brand" href="#"><img :src="company.logo" alt="Max-width 100%" style="height: 45px; "></a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavDropdown">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#"   @click.prevent="$router.push({ name: 'home' })">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#"   @click.prevent="$router.push({ name: 'about' })">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#"   @click.prevent="$router.push({ name: 'contact' })">Contact</a>
        </li>
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#"   @click.prevent="$router.push({ name: 'service' })">Service</a>
        </li>
        <li class="nav-item">
          <a class="nav-link active " aria-current="page" href="#"  @click.prevent="$router.push({ name: 'doctors' })">Doctors</a>
        </li>
        <div class="input-group rounded">
          <input type="search" class="form-control rounded" placeholder="Search" aria-label="Search" aria-describedby="search-addon" />
          <span class="input-group-text border-0" id="search-addon">
            <i class="fas fa-search"></i>
          </span>
        </div>
      </ul>
    </div>
  </div>
</nav>
    </div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
    name: "NavbarComponent",
    computed:{
      ...mapGetters({
        company : 'get_company'
      })
    }
    
}
</script>

<style scoped>


.appointment{
    color: #7F0000;
    background-color: white;
    font-weight: bold;
    padding: 0px 10px 0px 10px
}



</style>