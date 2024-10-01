<script>

import { RouterLink } from 'vue-router';

</script>

<template>

  <nav class="navbar navbar-expand-lg bg-body-tertiary">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">BOOTFOLIO</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link" :to="{name: 'home'}">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" :to="{name: 'projects'}">Progetti</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <div>
    <router-view></router-view>
  </div>

</template>

<style lang="scss">

</style>