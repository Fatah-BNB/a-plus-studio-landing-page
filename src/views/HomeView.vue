<template>
  <div class="home">

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
          class="w-fit text-white font-bold sm:text-xl px-10 py-5 bg-[#2539EC] rounded-full justify-center items-center">Contact
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

  </div>
</template>

<script>
import Header from "@/components/Header.vue"
import googleLogo from "./../assets/Google_Logo.svg"
import airbnbLogo from "./../assets/Airbnb_Logo.svg"
import UberEatsLogo from "./../assets/Uber_Eats_Logo.svg"
import Amazon_Logo from "./../assets/Amazon_Logo.svg"
export default {
  name: "HomeView",
  data: () => ({
    OurClientImgs: [
      { path: googleLogo, name: 'google' },
      { path: airbnbLogo, name: 'airbnb' },
      { path: UberEatsLogo, name: 'uber eats' },
      { path: Amazon_Logo, name: 'amazon' },
    ],
  }),
  components: {
    Header,
  },
  mounted() {
    document.title = "A+ Studio"
  }
};
</script>
