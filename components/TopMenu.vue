<template>
  <nav class="nav has-shadow">
    <div class="container">
      <!-- This "nav-toggle" hamburger menu is only visible on mobile -->
      <!-- You need JavaScript to toggle the "is-active" class on "nav-menu" -->
      <span class="nav-toggle">
        <span></span>
        <span></span>
        <span></span>
      </span>

      <!-- This "nav-menu" is hidden on mobile -->
      <!-- Add the modifier "is-active" to display it on mobile -->
      <div class="nav-left nav-menu">
        <a class="nav-item">
          <img src="https://nuxtjs.org/_nuxt/img/logo_nav.171838c.png" alt="nuxt logo">
        </a>
        <nuxt-link to="/" class="nav-item is-tab" active-class="is-active" exact>Home</nuxt-link>
        <nuxt-link to="/clients" class="nav-item is-tab" active-class="is-active" exact>Clients</nuxt-link>
        <nuxt-link to="/entries" class="nav-item is-tab" active-class="is-active" exact>Entries</nuxt-link>
        <nuxt-link to="/about" class="nav-item is-tab" active-class="is-active" exact>About page</nuxt-link>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'top-menu'
}
</script>

<style>

</style>
