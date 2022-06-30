<template>
  <nav id="menu" class="navbar navbar-expand-lg navbar-dark fixed-top p-0">
    <div class="container-fluid">
      <NuxtLink class="navbar-brand" to="/">
        <h1 class="m-0">Sebastian <span>X</span> Design</h1>
      </NuxtLink>
      <b-navbar-toggle class="button" target="nav-collapse">
        <template #default="{ expanded }">
          <font-awesome-icon v-if="expanded" icon="times" />
          <font-awesome-icon v-else icon="plus" />
        </template>
      </b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto d-flex align-items-center">
          <NuxtLink class="nav-link px-2 mx-2" to="/About">About</NuxtLink>
          <NuxtLink class="nav-link px-2 mx-2" to="/Contact">Contact</NuxtLink>
          <NuxtLink class="nav-link px-2 mx-2" to="carreraResume.pdf">Resume</NuxtLink>
        </b-navbar-nav>
      </b-collapse>
    </div>
  </nav>
</template>

<style lang="scss">
  .navbar {
    background-color: $dark;
    height: 50px;
    .navbar-brand {
      font-family: $axis-b;
      h1 {
        font-size: 1.55rem;
        padding: 0 8px;
        span {
          color: $blue;
        }
      }
    }
    .button {
      border-color: $dark !important;
      svg {width: 0.875em !important;}
    }
    #nav-collapse {
      background-color: $dark;
    }
    .nav-link {
      color: white !important;
      font-family: $lato-m;
      font-size: 1.2rem;
      @media (max-width: 991px) {
        font-size: 1rem;
        width: 100%;
        text-align: center;
      }
      &:hover {
        background-color: $light !important;
        color: black !important;
      }
    }
  }
</style>

<script>
export default {
  name: 'Header',
  components: { 
  }
}
</script>