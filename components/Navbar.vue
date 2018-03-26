<template>
  <div class="container">
    <nav class="navbar" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item" href="/">{{pkg.name}}</a>
        <button class="button navbar-burger" @click="showNav = !showNav">
          <span></span>
          <span></span>
          <span></span>
        </button>
      </div>
      <div class="navbar-menu" :class="{'is-active': showNav}">
        <div class="navbar-end">
          <nuxt-link class="navbar-item" to="/">Home</nuxt-link>
          <nuxt-link class="navbar-item" to="/about">About</nuxt-link>
          <nuxt-link class="navbar-item" to="/projects">Projects</nuxt-link>
          <nuxt-link class="navbar-item" to="/contact">Contact</nuxt-link>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
import pkg from "../package"
export default {
  data() {
    return {
      pkg,
			showNav: false
    }
  }
}
</script>
