<template>
  <div id="navbar">
    <v-app id="inspire">
      <div class="text-xs-center">
        <v-menu open-on-hover top offset-y>
          <template v-slot:activator="{ on }">
            <v-btn
              color="primary"
              dark
              v-on="on"
            >
              <img src="/french_flag.png" alt="french">
            </v-btn>
          </template>
    
          <v-list>
            <v-list-tile>
              <v-list-tile-title>
                <img src="/english_flag.svg" alt="english">
              </v-list-tile-title>
            </v-list-tile>
          </v-list>
        </v-menu>
      </div>
    </v-app>
  </div>
</template>
<script>
export default {
  name: 'navbarView',
}
</script>