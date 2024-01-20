<template>
    <div class="flex flex-col justify-center items-center">
        <div class="w-[70%] h-[1px] bg-[#E4E4E4] my-10"></div>
        <div class="flex flex-row gap-16 justify-evenly flex-wrap mx-20">
            <div id="a_plus_studio" class="flex flex-col md:w-[20%] gap-6 items-center md:items-start">
                <h3 class="flex flex-row gap-1"><span style="font-family: nova;" class="text-[1.3rem]">A+</span><span
                        class="text-[1.2rem]">Studio</span></h3>
                <p class="text-[#565656] md:text-[0.8rem]  text-[0.7rem] text-center md:text-start">Leading digital agency
                    with solid design and development expertise.
                    We build readymade websites, mobile
                    applications, and elaborate online business services.</p>
            </div>
            <div id="what_we_do" class="flex flex-col gap-6">
                <h3 class="font-bold md:text-[1.2rem] text-[1rem]">What we do</h3>
                <div class="flex flex-col gap-1">
                    <p class="md:text-[0.9rem] text-[0.8rem]">Web Design</p>
                    <p class="md:text-[0.9rem] text-[0.8rem]">App Design</p>
                    <p class="md:text-[0.9rem] text-[0.8rem]">Social Media Manage</p>
                    <p class="md:text-[0.9rem] text-[0.8rem]">Market Analysis Project</p>
                </div>
            </div>
            <div id="company" class="flex flex-col gap-6">
                <h3 class="font-bold md:text-[1.2rem] text-[1rem]">Company</h3>
                <div class="flex flex-col gap-1">
                    <p class="md:text-[0.9rem] text-[0.8rem]">About Us</p>
                    <p class="md:text-[0.9rem] text-[0.8rem]">Career</p>
                    <p class="md:text-[0.9rem] text-[0.8rem]">Become Investor</p>
                </div>
            </div>
            <div id="support" class="flex flex-col gap-6">
                <h3 class="font-bold md:text-[1.2rem] text-[1rem]">Support</h3>
                <div class="flex flex-col gap-1">
                    <p class="md:text-[0.9rem] text-[0.8rem]">FAQ</p>
                    <p class="md:text-[0.9rem] text-[0.8rem]">Policy</p>
                    <p class="md:text-[0.9rem] text-[0.8rem]">Business</p>
                </div>
            </div>
            <div id="contact" class="flex flex-col gap-6">
                <h3 class="font-bold md:text-[1.2rem] text-[1rem]">Contact</h3>
                <div class="flex flex-col gap-1">
                    <p class="md:text-[0.9rem] text-[0.8rem]">WhatsApp</p>
                    <p class="md:text-[0.9rem] text-[0.8rem]">Support 24</p>
                </div>
            </div>
        </div>
        <div class="flex flex-row gap-4 mt-10 w-[82%] justify-center lg:justify-start 2xl:w-[65%]">
            <img src="./../assets/facebook.png" alt="facebook">
            <img src="./../assets/twitter.png" alt="twitter">
            <img src="./../assets/linkedin.png" alt="linkedin">
        </div>
        <div class="my-10">
            <p class="text-center text-[#A4A4A4]">Copyright © 2022 Avi Yansah</p>
        </div>
    </div>
</template>
<script>
export default {
    name: 'FooterComponent',
}
</script>