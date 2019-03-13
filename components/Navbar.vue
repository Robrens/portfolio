<template>
  <div id="navbar">
    <ul v-if="this.$route.name =='lang-portfolio'">
      <li><a href="#about">Présentation</a></li>
      <li><a href="#techno">Connaissance</a></li>
      <li><a href="#project">Projets</a></li>
    </ul>
    <ul v-if="this.$route.name =='lang-portfolio'">
      <li><nuxt-link to="cv">Curiculum Vitae</nuxt-link></li>
      <li><nuxt-link to="contact">Contact</nuxt-link></li>
    </ul>
    <ul v-else-if="this.$route.name =='lang-cv'">
      <li><nuxt-link to="portfolio">Portfolio</nuxt-link></li>
      <li><nuxt-link to="contact">Contact</nuxt-link></li>
    </ul>
    <ul v-if="this.$route.name =='lang-contact'">
      <li><nuxt-link to="portfolio">Portfolio</nuxt-link></li>
      <li><nuxt-link to="cv">Curiculum Vitae</nuxt-link></li>
    </ul>
    <div class="swith-language" v-if="$route.params.lang == 'fr'">
      <div class="select-language"
      ref="button"
      @click="switchLanguage = !switchLanguage" 
      >
        <img src="/french_flag.png" alt="french">
        <button>↓</button>
      </div>
      <div class="language-choice"
      v-show="switchLanguage"
      v-closable="{
        exclude: ['button'],
        handler: 'onClose'
      }">
        <img src="/english_flag.png" alt="english" @click="toEnglish">
      </div>
    </div>
    <div class="swith-language" v-else>
      <div class="select-language"
        ref="button"
        @click="switchLanguage = !switchLanguage" 
      >
        <img src="/english_flag.png" alt="english">
        <button>↓</button>
      </div>
      <div class="language-choice"
      v-show="switchLanguage"
      v-closable="{
        exclude: ['button'],
        handler: 'onClose'
      }">
        <img src="/french_flag.png" alt="french" @click="toFrench">
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'navbarView',
  data () {
    return {
      switchLanguage: false
    }
  },
  methods: {
    onClose () {
      console.log(this.$route)
      this.switchLanguage = false
    },
    toEnglish () {
      const newPath = this.$route.path.substring(3)
      this.$router.go('/en/'+newPath)
    },
    toFrench () {
      const newPath = this.$route.path.substring(3)
      this.$router.go('/fr/'+newPath)
    }
  }
}
</script>
