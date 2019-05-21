<template>
  <section>
    <navbarView></navbarView>
    <v-layout>
      <v-flex text-xs-center>
        <aboutView></aboutView>
        <technoView></technoView>
        <projectView></projectView>
      </v-flex>
    </v-layout>
  </section>
</template>
<script>
  import navbarView from '~/components/Navbar.vue'
  import aboutView from '~/components/About.vue'
  import technoView from '~/components/Techno.vue'
  import projectView from '~/components/Project.vue'
  export default {
    components: {
      navbarView,
      aboutView,
      technoView,
      projectView
    }
  }

</script>
