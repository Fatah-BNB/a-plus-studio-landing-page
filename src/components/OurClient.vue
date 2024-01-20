<template>
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
</template>
<script>
import googleLogo from "./../assets/Google_Logo.svg"
import airbnbLogo from "./../assets/Airbnb_Logo.svg"
import UberEatsLogo from "./../assets/Uber_Eats_Logo.svg"
import Amazon_Logo from "./../assets/Amazon_Logo.svg"
export default {
    data: () => ({
        OurClientImgs: [
            { path: googleLogo, name: 'google' },
            { path: airbnbLogo, name: 'airbnb' },
            { path: UberEatsLogo, name: 'uber eats' },
            { path: Amazon_Logo, name: 'amazon' },
        ],
    })
}
</script>