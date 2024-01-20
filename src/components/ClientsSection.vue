<template>
    <div class="flex flex-col justify-center items-center">

        <div class="flex flex-col justify-center items-center text-center mb-40">
            <h1 class="text-black sm:text-[3rem] font-extrabold tracking-tight text-[2rem]">
                What our happy client say</h1>
            <p class="text-base text-center text-neutral-600 lg:text-[1rem]">Several selected clients, who already
                believe in our service.</p>
        </div>

        <div class="w-[80%] hidden lg:flex lg:flex-row justify-around">
            <div class="1/3 relative">
                <img src="./../assets/Dots.svg" alt="dots" class="absolute -z-10 -top-10 -right-10">
                <img src="./../assets/Empty_Ellipse.svg" alt="ellipse" class="absolute -z-10 bottom-0">
                <img src="./../assets/matthew_paul.png" alt="photo" class="rounded-l-full rounded-br-full shadow-2xl">
            </div>
            <swiper class=" w-1/2" :slides-per-view="1" :space-between="30" :loop="true" :pagination="true"
                :navigation="false" :autoplay="{ delay: 3000, disableOnInteraction: false }">
                <swiper-slide v-for="(feedback, index) in feedbacks" :key="index">
                    <div class="flex justify-center items-center relative">
                        <div class="flex flex-col space-y-10 w-[50%] xl:m-10 lg:m-0 md:w-[80%]">
                            <h1 class="font-bold text-2xl text-center">{{ feedback.name }}</h1>
                            <p class="text-center">{{ feedback.comment }}</p>
                        </div>
                    </div>
                </swiper-slide>
            </swiper>
            <div class="w-1/3 relative">
                <img src="./../assets/about_us_Ellipse.svg" alt="ellipse"
                    class="absolute -z-10 xl:bottom-16 xl:left-16 lg:bottom-32 lg:left-10">
                <img src="./../assets/people.png" alt="photo">
            </div>
        </div>
        <div class="w-[85%] lg:hidden block">
            <swiper :slides-per-view="1" :space-between="30" :loop="true" :pagination="true" :navigation="false"
                :autoplay="{ delay: 3000, disableOnInteraction: false }">
                <swiper-slide v-for="(feedback, indexe) in feedbacks" :key="indexe">
                    <div class="flex flex-col justify-between items-center">
                        <img :src="feedback.picture" :alt="feedback.name" class="rounded-full shadow-xl w-1/2">
                        <div class="flex flex-col space-y-10 justify-center items-center my-10">
                            <h1 class="font-bold text-2xl">{{ feedback.name }}</h1>
                            <p class="text-center">{{ feedback.comment }}</p>
                        </div>
                    </div>
                </swiper-slide>
            </swiper>
        </div>
    </div>
</template>
<script>
import { Navigation, Pagination, Autoplay } from 'swiper';

import { SwiperCore, Swiper, SwiperSlide } from 'swiper-vue2'

// Import Swiper styles
import 'swiper/swiper-bundle.css'

SwiperCore.use([Navigation, Pagination, Autoplay])
import MatthewPaul from "./../assets/matthew_paul.png"
export default {
    data: () => ({
        feedbacks: [
            { name: 'Matthew Paul', comment: 'Perfect, very good job! Thank you for the amazing design and work. Really impressed with the high quality and quick turnaround time. Highly recommend.', picture: MatthewPaul },
            { name: 'Matthew Paul', comment: 'Perfect, very good job! Thank you for the amazing design and work. Really impressed with the high quality and quick turnaround time. Highly recommend.', picture: MatthewPaul },
            { name: 'Matthew Paul', comment: 'Perfect, very good job! Thank you for the amazing design and work. Really impressed with the high quality and quick turnaround time. Highly recommend.', picture: MatthewPaul },
        ]
    }),
    components: {
        Swiper,
        SwiperSlide
    },
    methods: {
    }
}
</script>