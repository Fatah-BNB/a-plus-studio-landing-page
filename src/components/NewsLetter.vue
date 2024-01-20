<template>
    <div class="my-48">
        <div id="outer_container" class="flex justify-center">
            <div id="container"
                class="relative w-[80%] xl:h-[300px] rounded-[75px] xl:shadow-sm shadow-lg bg-[#F4F9FF] xl:space-y-0 sm:space-y-16  flex xl:flex-row flex-col sm:gap-16 sm:p-0 p-10 gap-10 justify-center items-center">
                <img src="./../assets/Rectangle.svg" alt="rectangle"
                    class="absolute -z-10 -left-10 -bottom-10 rounded-bl-[100px]">
                <img src="./../assets/dots_square.svg" alt="rectangle" class="absolute -z-10 -right-10 xl:-top-16 -top-32">
                <div id="content" class="w-1/2 flex justify-center items-center">
                    <div class="space-y-5">
                        <h1 class="text-black sm:text-[3rem] font-extrabold tracking-tight text-[2rem] text-center">
                            Subscribe Newsletter
                        </h1>
                        <p class="text-center text-[#757575]">I will update good news and promotion service not spam</p>
                    </div>
                </div>
                <div id="input_outer_container" class="xl:w-1/2 h-full flex justify-center items-center relative">
                    <img src="./../assets/newsletter_rectangle.svg" alt="rectangle"
                        class="hidden xl:block absolute xl:w-4/4 h-full right-0">
                    <div class="xl:z-20">
                        <div id="input_container"
                            class="sm:shadow-xl flex sm:flex-row flex-col gap-28 justify-between items-center sm:bg-white rounded-[60px] xl:p-0 sm:pl-16 mb-16 xl:mb-0">
                            <input type="text" placeholder="Enter your email address.."
                                class="outline-none rounded-full xl:pl-3 2xl:pl-7 p-5 sm:p-0 shadow-xl sm:shadow-none">
                            <button
                                class="sm:m-3 w-fit text-white p-3 font-bold lg:text-[1rem] xl:text-[1rem] xl:px-10 xl:py-5 lg:py-5 lg:px-5 bg-[#2539EC] rounded-full justify-center items-center">Contact
                                Now</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>