<template>
  <div id="navbar">
    <select>
      <option value="" class="navbar-item-french" default>
      </option>
      <option value="">
        <nuxt-link class="navbar-item-english" to="/en/portfolio">
        </nuxt-link>
      </option>
    </select>
  </div>
</template>
<script>
export default {
  name: 'navbarView',
  data () {
    return {
      french: require("@/static/french_flag.png"),
      english: require("@/static/english_flag.svg")
    }
  },
  methods: {
    toEnglish () {
      this.$router.push('/en/portfolio')
    }
  }
}
</script>