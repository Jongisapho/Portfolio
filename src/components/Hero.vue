<template>
    <section class="relative w-full overflow-hidden min-h-screen flex items-center bg-slate-950">
        <div class="text-white w-full max-w-5xl lg:max-w-7xl mx-auto relative z-10">
            <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
                <div class="flex flex-col justify-center lg:-mt-40 mt-5 p-5">
                    <div class="text-white lg:text-center" data-aos="fade-right">
                    <h1 class="font-bold md:text-4xl text-5xl">
                        Hello, I'm
                        <span
                            class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 via-red-200 to-cyan-600">Jongisapho
                            Ndeya</span>

                    </h1>
                    <p class="font-medium text-xl md:text-xl mt-5" data-aos="fade-right" data-aos-delay="500">
                        Computer Scientist | Software Developer | AI & ML Engineering
                    </p>
                </div>
                <p class="text-gray-200 text-center mx-auto max-w-xl text-lg leading-relaxed mt-10 mr-10 lg:mx-0">
                    I am a Computer Science graduate, A Computer Science Honours student with an obession for Software Engineering, Machine Learning and Natural Language Processing.
                    I enjoy building blazing-fast, scalable full-stack applications.
                    I love writing clean, efficient code that solves real problems and I do it with focus, speed and enthusiasm.
                </p>
                <div class="flex items-center gap-4 flex-col sm:flex-row sm:w-max sm:mx-auto mt-10"
                    data-aos="fade-up" data-aos-delay="300">
                    <CustomButton
                        label="Contact me"
                        variant="primary"
                        @click="handleContact"
                    >
                        <template #icon-right>
                            <ArrowRightIcon class="ml-2 w-5 h-5 group-hover:translate-x-2 transition-transform duration-600" />
                        </template>
                    </CustomButton>


                    <CustomButton label="Download CV" variants="secondary" @click="handleDownloadCV">
                        <template #icon-left>
                            <ArrowDownTrayIcon class="w-6 h-6 mr-2 text-white group-hover-translate-y-1 transition-transform duration-500" />
                        </template>
                    </CustomButton>
                </div>
                </div>
                <div class="flex items-center justify-center lg:justify-start gap-8 md:ml-30 pt-4" data-aos="fade-up"
                    data-aos-delay="400">
                    <div class="lg:h-full flex justify-center lg:justify-end">
                        <div class="relative w-full max-w-md lg:max-w-lg">
                            <div class="relative z-10 bg-linear-to-r from-cyan-600 via-red-200 to-cyan-600 shadow-2xl rounded-[50%_40%_30%_60%/60%_30%_70%_30%]
                            p-4 backdrop-blur-sm border border-blue-500/30
                            -translate-y-6"
                            data-aos="zoom-in"
                            data-aos-delay="500">
                                <div class="rounded-xl overflow-hidden">
                                    <img src="/hero.png" alt="Jongisapho - Software Engineer"
                                    loading="lazy"
                                    class="w-[500px]. h-125 object-contain -translate-y-8">

                                </div>
                            </div>
                        
                            <div class="absolute -top-2 -right-4 w-10 h-10 bg-blue-400 rounded-full blur-sm opacity-6 animate-pulse">
                                
                            </div>
                        </div>

                    </div>

                </div>

            </div>
        </div>

    </section>
</template>

<script setup>

import { ArrowRightIcon, ArrowDownTrayIcon } from '@heroicons/vue/16/solid';
import CustomButton from './CustomButton.vue'

const handleContact = () => {
    console.log("Contact clicked");
}

const handleDownloadCV = () => {
    console.log("Download CV clicked");
}

</script>

<style>

</style>