<template>
  <nav class="navbar navbar-expand-lg fixed-top navbar-dark bg-dark">
    <nuxt-link to="/" class="navbar-brand">Nuxt App</nuxt-link>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarNavDropdown"
      aria-controls="navbarNavDropdown"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavDropdown">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <nuxt-link to="/" class="nav-link">
            <i class="fas fa-home"></i> Home
          </nuxt-link>
        </li>
        <li class="nav-item">
          <nuxt-link to="/users" class="nav-link">
            <i class="fas fa-users"></i> Users
          </nuxt-link>
        </li>
      </ul>
    </div>
  </nav>
</template>
