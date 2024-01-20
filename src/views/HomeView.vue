<template>
  <div class="home animate-fadeUp">

    <Header />

    <HeroHeadline />

    <OurClient />

    <Services />

    <AboutUs />

    <ClientsSection />

    <NewsLetter />

    <Footer />

  </div>
</template>

<script>
import Header from "@/components/Header.vue"
import Footer from "@/components/Footer.vue"
import HeroHeadline from "@/components/HeroHeadline.vue"
import OurClient from "@/components/OurClient.vue"
import Services from "@/components/Services.vue"
import AboutUs from "@/components/AboutUs.vue"
import NewsLetter from "@/components/NewsLetter.vue"
import ClientsSection from "@/components/ClientsSection.vue"
export default {
  name: "HomeView",
  components: {
    Header,
    HeroHeadline,
    OurClient,
    Services,
    AboutUs,
    ClientsSection,
    NewsLetter,
    Footer
  },
  mounted() {
    document.title = "A+ Studio"
  }
};
</script>
