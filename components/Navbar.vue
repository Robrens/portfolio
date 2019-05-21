<template>
  <div id="navbar">
    <ul v-if="this.$route.name =='lang-portfolio'">
      <li><a href="#about">Présentation</a></li>
      <li><a href="#techno">Connaissance</a></li>
      <li><a href="#project">Projets</a></li>
    </ul>
    <div class="cv">
      <a href="">download CV</a>
    </div>
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
      <router-link to="/en/portfolio">
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
      <router-link to="/fr/portfolio">
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
