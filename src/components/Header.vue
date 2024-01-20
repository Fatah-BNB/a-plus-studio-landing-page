<template>
  <div class="md:mx-[8%] md:my-11">
    <header id="top-menu" class="flex flex-row justify-between md:items-center">
      <div class="w-[10%] lg:w-[7%] md:w-[3%] flex flex-row md:justify-center md:py-0 py-5 md:px-0 px-10">
        <span style="font-family: nova;" class="lg:text-[1.5rem] md:text-[1.3rem] md:pr-1 text-[2rem]">A+</span><span
          class="lg:text-2xl md:text-xl md:pl-1 leading-normal md:leading-2 text-3xl">Studio</span>
      </div>
      <nav id="nav-options relative my-10">
        <ul
          :class="{ 'translate-x-0 translate-y-[25%]': menuToggle, '-translate-x-[100%] translate-y-[25%] md:translate-y-0': !menuToggle, }"
          class="py-5 bg-white left-0 md:translate-x-0 flex md:flex-row  md:h-full z-10 md:static absolute flex-col w-full items-center space-y-6 md:space-y-0 transition-transform duration-300 ease-in-out">
          <li v-for="route in routes" :key="route.name" @click="toggleMenu"
            class="hover:bg-black 2xl:px-12 lg:px-8 md:px-5 hover:text-white transition-all text-base font-extrabold flex md:items-center">
            <router-link :to="route.path">{{ route.name }}</router-link>
          </li>
        </ul>
      </nav>
      <div class="md:hidden w-16 self-center cursor-pointer" @click="toggleMenu">
        <img src="./../assets/menu.svg" alt="menu" :class="{ 'hidden': menuToggle }" class="w-[50%]">
        <img src="./../assets/close.svg" alt="close" :class="{ 'hidden': !menuToggle }" class="w-[50%]">
      </div>
    </header>
  </div>
</template>
<script>
export default {
  name: "HeaderComponent",
  data: () => ({
    menuToggle: false,
    routes: [
      { path: "/", name: "Home" },
      { path: "/what-we-do", name: "What We Do" },
      { path: "/services", name: "Services" },
      { path: "/project", name: "Project" },
      { path: "/blog", name: "Blog" },
      { path: "/contact", name: "Contact" },
    ],
  }),
  methods: {
    toggleMenu() {
      this.menuToggle = !this.menuToggle
    }
  }
};
</script>
