<template>
  <div id="navbar">
    <ul>
      <li><a href="#about">Présentation</a></li>
      <li><a href="#techno">Connaissance</a></li>
      <li><a href="#project">Projets</a></li>
    </ul>
    <ul>
      <li><a href="">Curiculum Vitae</a></li>
      <li><a href="">Contact</a></li>
    </ul>
    <div class="swith-language" v-if="$route.path == '/fr/portfolio' || $route.path == '/fr/cv' || $route.path == '/fr/contact'">
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
        <nuxt-link class="navbar-item-english" to="/en/portfolio">
          <img src="/english_flag.png" alt="english">
        </nuxt-link>
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
        <nuxt-link class="navbar-item-french" to="/fr/portfolio">
          <img src="/french_flag.png" alt="french">
        </nuxt-link>
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
      this.switchLanguage = false
    }
  }
}
</script>
