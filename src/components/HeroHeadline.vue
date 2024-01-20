<template>
    <div id="hero-headline" class="lg:grid lg:grid-cols-2 2xl:mt-10">

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
</template>