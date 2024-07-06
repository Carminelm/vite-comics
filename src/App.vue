<script>
import AppHeader from './components/header/AppHeader.vue';
import MainJumbotron from './components/main/MainJumbotron.vue';
import MainNavbar from './components/main/MainNavbar.vue';
import FooterNavbar from './components/footer/FooterNavbar.vue';
import FooterSocialLinks from './components/footer/FooterSocialLinks.vue';



export default {
  components: {
    AppHeader,
    MainJumbotron,
    MainNavbar,
    FooterNavbar,
    FooterSocialLinks,
  }
}
</script>

<template>
  <AppHeader />


  <main>
    <MainJumbotron />
    <MainNavbar />
  </main>


  <footer>
    <FooterNavbar />
    <FooterSocialLinks />
  </footer>
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables' as *;


body {
  color: $primary--color;
}
</style>