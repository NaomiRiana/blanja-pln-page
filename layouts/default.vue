<template>
  <div>
    <section class="before-page">
      <Header />
      <Banner />
    </section>
    <section class="main-page">
      <!-- <div class="page-container">
        <div class="page-wrapper"> -->
          <nuxt />
        <!-- </div>
      </div> -->
    </section>
    <section class="after-page">
      <FooterMenu />
      <Footer />
    </section>
  </div>
</template>

<script>
import Header from "~/components/Header/Header";
import Banner from "~/components/Body/Banner";
import FooterMenu from '~/components/Footer/FooterMenu';
import Footer from '~/components/Footer/Footer';
export default {
  components: {
    Header, Banner, FooterMenu, Footer
  }
}
</script>

<style lang="scss">
   @import '../assets/css/style.scss';
</style>