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
      <router-link v-if="$route.fullPath === '/fr/portfolio'" to="/en/portfolio">
        <img src="/english_flag.png" alt="english">
      </router-link>
      <router-link v-else-if="$route.fullPath === '/fr/cv'" to="/en/cv">
        <img src="/english_flag.png" alt="english">
      </router-link>
      <router-link v-else to="/en/contact">
        <img src="/english_flag.png" alt="english">
      </router-link>
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
      <router-link v-if="$route.fullPath === '/en/portfolio'" to="/fr/portfolio">
        <img src="/french_flag.png" alt="french">
      </router-link>
      <router-link v-else-if="$route.fullPath === '/en/cv'" to="/fr/cv">
        <img src="/french_flag.png" alt="french">
      </router-link>
      <router-link v-else to="/fr/contact">
        <img src="/french_flag.png" alt="french">
      </router-link>
      </div>
    </div>
  </div>
</template>
<script>
import { i18n } from '@/plugins/i18n.js'
import { log } from 'util';
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
    }
  }
}
</script>
