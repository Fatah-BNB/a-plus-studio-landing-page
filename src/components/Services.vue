<template>
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
                <h1 class="text-black sm:text-[3rem] font-extrabold tracking-tight text-[2rem]">How can we help your
                    Business ?
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
</template>
<script>
import emptyWallet from "./../assets/empty_wallet.svg"
import searchBox from "./../assets/box_search.svg"
import chartSquare from "./../assets/chart_square.svg"
import code from "./../assets/code.svg"
export default {
    name: 'ServicesComponent',
    data: () => ({
        services: [
            { title: 'Business Idea Planning', desc: 'We present you a proposal and discuss niffty-gritty like', icon: searchBox, color: '#f1f7ff' },
            { title: 'Development Website and App', desc: 'Communication protocols apart from engagement models', icon: code, color: '#fff2f8' },
            { title: 'Financial Planning System', desc: 'Protocols apart from aengage models, pricing billing', icon: emptyWallet, color: '#fff7e3' },
            { title: 'Market Analysis Project', desc: 'Protocols apart from aengage models, pricing billing', icon: chartSquare, color: '#deffee' }
        ]
    })

}
</script>