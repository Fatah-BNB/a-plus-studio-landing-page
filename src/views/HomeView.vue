<template>
  <div class="home animate-fadeUp">

    <Header />

    <div id="hero-headline" class="lg:grid lg:grid-cols-2 2xl:mt-20">

      <div id="hero-headline-content" class="relative flex justify-center items-center">

        <div class="lg:w-[70%] lg:flex lg:flex-col lg:space-y-10 hidden">
          <h1 class="text-black text-[3rem] font-extrabold tracking-tight">A Digital Product Agency</h1>
          <P class="text-base tracking-wide text-neutral-600 pr-24">Leading digital agency with solid design and
            development expertise. We build readymade websites, mobile applications, and elaborate online business
            services.</P>
          <button
            class="w-fit text-white font-bold text-xl px-10 py-5 bg-[#2539EC] rounded-full justify-center items-center">Contact
            Now</button>
        </div>

        <img src="./../assets/Dot_Ornament.svg" alt="dots"
          class="absolute -z-10 md:bottom-0 lg:left-16 lg:translate-y-20 hidden lg:block xl:translate-y-16 2xl:-translate-y-10 2xl:translate-x-20">

      </div>

      <div class="relative">
        <img src="./../assets/hero_headline_img.png" alt="hero_headline_img"
          class="w-full lg:h-full lg:object-cover lg:rounded-bl-[200px]" />
        <img src="./../assets/Ellipse.svg" alt="elipse"
          class="sm:hidden md:block md:w-fit w-full -bottom-2 translate-y-96 translate-x-0 absolute -z-10 lg:top-0 lg:left-0 lg:-translate-x-16 lg:-translate-y-0 sm:translate-y-3 sm:translate-x-22 md:bottom-0 md:translate-y-20">
        <img src="./../assets/Rectangle.svg" alt="rectangle"
          class="rounded-br-[100px] absolute -z-10 sm:bottom-0 sm:right-0 sm:-translate-x-10 sm:translate-y-24 sm:block hidden">
      </div>

      <div class="flex flex-col space-y-10 justify-center items-center mt-10 lg:hidden">
        <h1 class="w-[75%] text-black text-center text-[2rem] sm:text-[3rem] font-extrabold tracking-tight">A Digital
          Product Agency</h1>
        <P class="w-[80%] text-base tracking-wide text-center text-neutral-600">Leading digital agency with solid design
          and
          development expertise. We build readymade websites, mobile applications, and elaborate online business
          services.</P>
        <button
          class="hover:bg-white hover:text-[#2539EC] hover:border hover:border-[rgba(0, 0, 0, 0.5)] transition-all w-fit text-white font-bold sm:text-xl px-10 py-5 bg-[#2539EC] rounded-full justify-center items-center">Contact
          Now</button>
      </div>

    </div>

    <div id="our-client" class="flex lg:flex-row w-full justify-center items-center my-48 flex-col">
      <div class="w-[83%] flex xl:flex-row xl:space-x-16 flex-col justify-center items-center space-y-16">
        <div class="xl:flex xl:flex-col space-y-4 xl:w-[25%] w-[80%] text-center xl:text-left">
          <h1 class="text-black sm:text-[3rem] font-extrabold tracking-tight text-[2rem]">Our Client</h1>
          <p class="text-base tracking-wide text-neutral-600">Several selected clients, who already believe in our
            service.
          </p>
        </div>
        <div
          class="md:flex md:flex-row md:space-x-[5%] lg:space-x-[10%] xl:space-x-16 md:items-center md:justify-center grid grid-cols-2 gap-10 xl:w-[70%]">
          <img v-for="image in OurClientImgs" :key="image.name" :src="image.path" :alt="image.name"
            class="lg:w-44 md:w-36" />
        </div>
      </div>
    </div>


    <div id="services" class="flex lg:flex-row w-full justify-center items-center my-48 flex-col relative">
      <img src="./../assets/Big_Rectangle.svg" alt="rectangle"
        class="xl:rounded-tl-[150px] -z-10 absolute 2xl:w-[72%] xl:w-[70%] 2xl:top-32 right-0 hidden xl:block">
      <img src="./../assets/services_dots.svg" alt="dots"
        class="absolute -z-20 xl:top-[100%] xl:bottom-10 xl:left-32 hidden xl:translate-x-0 xl:-translate-y-[100%] md:block md:top-[50%] md:left-[50%] md:translate-y-[50%] md:-translate-x-[50%]">
      <div class="w-[83%] flex xl:flex-row xl:space-x-16 flex-col justify-center items-center">
        <div id="service-content"
          class="xl:flex xl:flex-col space-y-4 xl:w-[35%] w-[80%] text-center xl:text-left relative">
          <img src="./../assets/Rectangle.svg" alt="rectangle"
            class="absolute rounded-tl-[100px] xl:w-[50%] -z-10 xl:left-0 xl:bottom-0 xl:-translate-x-14 2xl:-translate-y-14 xl:-translate-y-44 hidden md:block md:-translate-y-24">
          <h1 class="text-black sm:text-[3rem] font-extrabold tracking-tight text-[2rem]">How can we help your Business ?
          </h1>
          <p class="text-base tracking-wide text-neutral-600">We build readymade websites, mobile applications, and
            elaborate online business services.
          </p>
        </div>
        <div class="relative flex flex-col ml-0 space-y-10
          md:flex-row md:justify-around md:w-full
          lg:justify-center lg:w-full lg:space-x-10 
          xl:w-[70%] ">
          <img src="./../assets/Empty_Ellipse.svg" alt="ellipse"
            class="absolute -z-20 xl:translate-x-[200%] xl:translate-y-[220%] hidden lg:block lg:top-[50%] lg:left-[50%] lg:-translate-x-10 lg:-translate-y-10">
          <div id="cards-container" class="flex flex-col justify-center items-center space-y-10">
            <div v-for="service in services.slice(0, services.length / 2)" :key="service.title"
              class="border border-[rgba(0, 0, 0, 0.5)] w-[300px] h-[350px] shadow-lg bg-white rounded-[25px] flex flex-col justify-center items-center p-4 space-y-6">
              <div :style="{ 'background-color': service.color }"
                class="w-[120px] h-[120px] rounded-3xl flex justify-center items-center p-6">
                <img :src="service.icon" :alt="service.title">
              </div>
              <h3 class="font-bold text-xl w-[55%] text-center">{{ service.title }}</h3>
              <p class="w-[80%] tracking-wide text-neutral-600 text-center">{{ service.desc }}</p>
            </div>

          </div>
          <div id="cards-container" class="flex flex-col items-center space-y-10 xl:pb-28">
            <div v-for="service in services.slice(services.length / 2, services.length)" :key="service.title"
              class="border border-[rgba(0, 0, 0, 0.5)] w-[300px] h-[350px] shadow-lg bg-white rounded-[25px] flex flex-col justify-center items-center p-4 space-y-6">
              <div :style="{ 'background-color': service.color }"
                class="w-[120px] h-[120px] rounded-3xl flex justify-center items-center p-6">
                <img :src="service.icon" :alt="service.title">
              </div>
              <h3 class="font-bold text-xl w-[55%] text-center">{{ service.title }}</h3>
              <p class="w-[80%] text-center text-neutral-600">{{ service.desc }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div id="about-us" class="flex lg:flex-row w-full justify-center items-center my-48 flex-col">
      <div class="w-[85%] flex flex-col lg:flex-row justify-center items-center lg:space-x-24">
        <div class="relative xl:w-1/2 lg:w-[65%]">
          <img src="./../assets/about_us_img.png" alt="about-us-img" class="rounded-[32px] shadow-2xl">
          <img src="./../assets/about_us_Ellipse.svg" alt="ellipse"
            class="absolute right-0 bottom-0 -z-10 lg:translate-y-10 lg:translate-x-10 hidden lg:block">
          <img src="./../assets/play_button.svg" alt="play"
            class="absolute z-10 top-[50%] left-[50%] -translate-x-[50%] -translate-y-[50%]">
        </div>
        <div id="about-us_content" class="relative flex flex-col 2xl:space-y-14 space-y-8 xl:w-1/2 lg:w-[50%] w-full">
          <img src="./../assets/about_us_Rectangle.svg" alt="rectangle"
            class="absolute -z-10 rounded-br-[100px] top-0 left-0 lg:-translate-x-6 lg:-translate-y-10 xl:-translate-y-18 2xl:-translate-y-10 md:-translate-y-16 md:-translate-x-5 hidden md:block">
          <h1
            class="text-black text-center md:text-start text-[2rem] lg:text-[2rem] sm:text-[3rem] font-extrabold tracking-tight">
            Great
            Digital Product Agency since 2016</h1>
          <P class="text-base text-center md:text-start text-neutral-600 lg:text-[1rem]">Our Business Plan is a written
            document
            describing a company's core business activites, Objectives, and how it plans to achieve its goals. Our goal is
            to provide our client high quality Product with modern idea accordingly their budgets and according thir
            reuirements.</P>
        </div>
      </div>
    </div>

    <div class="flex flex-col justify-center my-40">
      <h1 class="text-black text-center text-[2rem] lg:text-[2rem] sm:text-[3rem] font-extrabold tracking-tight">
        What our happy client say</h1>
      <p class="text-base text-center text-neutral-600 lg:text-[1rem]">Several selected clients, who already
        believe in our service.</p>
    </div>
    <ClientsSection />

    <div class="my-48 flex flex-col justify-center items-center">
      <img src="./../assets/Newsletter.png" alt="newsletter" class="w-3/4">
    </div>

    <div class="flex flex-col justify-center items-center">
      <img src="./../assets/Footer.png" alt="footer" class="w-3/4">
    </div>


  </div>
</template>

<script>
import Header from "@/components/Header.vue"
import googleLogo from "./../assets/Google_Logo.svg"
import airbnbLogo from "./../assets/Airbnb_Logo.svg"
import UberEatsLogo from "./../assets/Uber_Eats_Logo.svg"
import Amazon_Logo from "./../assets/Amazon_Logo.svg"
import emptyWallet from "./../assets/empty_wallet.svg"
import searchBox from "./../assets/box_search.svg"
import chartSquare from "./../assets/chart_square.svg"
import code from "./../assets/code.svg"
import ClientsSection from "@/components/ClientsSection.vue"
export default {
  name: "HomeView",
  data: () => ({
    OurClientImgs: [
      { path: googleLogo, name: 'google' },
      { path: airbnbLogo, name: 'airbnb' },
      { path: UberEatsLogo, name: 'uber eats' },
      { path: Amazon_Logo, name: 'amazon' },
    ],
    services: [
      { title: 'Business Idea Planning', desc: 'We present you a proposal and discuss niffty-gritty like', icon: searchBox, color: '#f1f7ff' },
      { title: 'Development Website and App', desc: 'Communication protocols apart from engagement models', icon: code, color: '#fff2f8' },
      { title: 'Financial Planning System', desc: 'Protocols apart from aengage models, pricing billing', icon: emptyWallet, color: '#fff7e3' },
      { title: 'Market Analysis Project', desc: 'Protocols apart from aengage models, pricing billing', icon: chartSquare, color: '#deffee' }
    ]
  }),
  components: {
    Header,
    ClientsSection
  },
  mounted() {
    document.title = "A+ Studio"
  }
};
</script>
