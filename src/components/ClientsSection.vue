<template>
    <div class="w-full flex justify-center">
        <div class="w-[85%] hidden lg:block">
            <swiper :slides-per-view="1" :space-between="30" :loop="true" :pagination="true" :navigation="true"
                :autoplay="{ delay: 3000, disableOnInteraction: false }">
                <swiper-slide v-for="(feedback, indexe) in feedbacks" :key="indexe">
                    <div class="flex flex-row justify-between items-center space-x-20">
                        <img :src="feedback.picture" :alt="feedback.name"
                            class="rounded-l-full rounded-br-full shadow-xl w-1/2">
                        <div class="flex flex-col space-y-10 w-3/4 mb-40">
                            <h1 class="font-bold text-2xl">{{ feedback.name }}</h1>
                            <p class="w-1/2">{{ feedback.comment }}</p>
                        </div>
                    </div>
                </swiper-slide>
            </swiper>
        </div>
        <div class="w-[85%] lg:hidden block">
            <swiper :slides-per-view="1" :space-between="30" :loop="true" :pagination="true" :navigation="true"
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