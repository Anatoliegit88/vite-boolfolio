<script>
export default {
  name: "AppHeader",
};
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      <router-link class="navbar-brand" :to="{ name: 'home' }"
        >MyProjects</router-link
      >
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarNavDropdown"
        aria-controls="navbarNavDropdown"
        aria-expanded="false"
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav">
          <li class="nav-item active">
            <router-link class="nav-link" :to="{ name: 'home' }"
              >Home<span class="sr-only"></span
            ></router-link>
          </li>

          <li class="nav-item active">
            <router-link class="nav-link" :to="{ name: 'about-us' }"
              >About Us<span class="sr-only"></span
            ></router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
