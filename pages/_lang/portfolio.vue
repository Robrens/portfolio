<template>
  <section>
    <navbarView></navbarView>
    <v-layout>
      <v-flex text-xs-center>
        <div id="about">
          <h2 class="title">Présentation</h2>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta inventore reiciendis, eum animi ea tenetur accusantium adipisci? Rem, ducimus at tempora cum autem sit quos officiis! Nulla, mollitia illum? Quam?</p>
        </div>
        <div id="techno">
          <h2 class="title">technologies</h2>
          <ul>
            <li>plop</li>
            <li>plop</li>
            <li>plop</li>
            <li>plop</li>
            <li>plop</li>
            <li>plop</li>
            <li>plop</li>
            <li>plop</li>
          </ul>
        </div>
        <div id="project">
          <h2 class="title">réalisations</h2>
          <p>In coming</p>
        </div>
      </v-flex>
    </v-layout>
  </section>
</template>
<script>
import navbarView from '~/components/Navbar.vue'
export default {
  components: {
    navbarView
  }
}
</script>
