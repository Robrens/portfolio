<template>
  <v-layout align-center justify-space-around row fill-height>
    <v-flex
      xs12
      sm8
      md6
    >
      <div class="language-choice">
        <nuxt-link class="navbar-item" to="/fr/portfolio">
          <img src="/french_flag.png" alt="french">
        </nuxt-link>
        <nuxt-link class="navbar-item" to="/en/portfolio">
          <img src="/english_flag.svg" alt="english">
        </nuxt-link>
      </div>
    </v-flex>
  </v-layout>
</template>

<script>

export default {
  
  }
</script>
