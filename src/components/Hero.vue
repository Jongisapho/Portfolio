<template>
    <section class="relative w-full overflow-hidden min-h-screen flex items-center pt-7 bg-slate-950">
        <div class="text-white w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto relative z-10">
            <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center ">
                <div class="text-lg lg:text-left" data-aos="fade-right">
                    <h1 class="font-bold md:text-4xl text-3xl">
                        Hello, I'm
                        <span
                            class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 via-red-200 to-cyan-600">Jongisapho
                            Ndeya</span>

                    </h1>
                    <p class="font-medium text-lg md:text-xl mt-4" data-aos="fade-right" data-aos-delay="500">
                        Computer Science Graduate | Software Developer | AI Engineering Enthusiast
                    </p>
                </div>
                <p class="pt-5 lg:text-left mx-auto max-w-xl text-lg leading-relaxed"
                    data-aos="fade-left">
                    I am BSc Computer Science Graduate and I am currently enrolled for my BScHons in Computer Science at
                    the University of Pretoria.
                    I am passionate about building scalable and data-driven systems. I am proficient in Java, C++,
                    Python, JavaScript and modern frameworks including Vue, React, Node.js and Spring Boot
                </p>
                <div class="flex items-center gap-4 pt-8 flex-col sm:flex-row sm:w-max sm:mx-auto lg:mx-0"
                    data-aos="fade-up" data-aos-delay="300">
                    <button class="px-8 md:px-10 md:py-2 py-3 rounded-full relative group w-full
                sm:w-max flex justify-center ocerflow-hidden bg-linear-to-r from-blue-400 via-red-200 to-cyan-600
                transition-all
                duration-300 hover:scale-105">
                        <span class="relative flex items-center justify-center text-white font-semibold text-lg">
                            Contact me
                            <ArrowRightIcon
                                class="ml-2 w-5 h-5 group-hover:translate-x-2 transition-transform duration-600" />
                        </span>
                    </button>
                    <button class="px-8 md:px-10 md:py-2 py-3 rounded-full relative group w-full
                sm:w-max flex justify-center ocerflow-hidden bg-linear-to-r from-blue-400 via-red-200 to-cyan-600
                transition-all
                duration-300 hover:scale-105">
                        <div class="flex items-center justify-center relative">
                            <ArrowDownTrayIcon
                                class="w-6 h-6 text-white group-hover:translate-y-1 transition-transform duration-500" />
                            <span class="text-white pl-3 font-semibold text-lg"> Download CV</span>
                        </div>
                    </button>
                </div>
                <div class="flex items-center justify-center lg:justify-start gap-8 pt-12" data-aos="fade-up"
                    data-aos-delay="400">
                    <div class="lg:h-full flex justify-center lg:justify-end">
                        <div class="relative w-full max-w-md lg:max-w-lg">
                            <div class="relative z-10 bg-linear-to-r from-blue-400 via-red-200 to-cyan-600 shadow-2xl rounded-[50%_40%_30%_60%/60%_30%_70%_30%]
                            p-4 backdrop-blur-sm border border-blue-500/30
                            -translate-y-6"
                            data-aos="zoom-in"
                            data-aos-delay="500">
                                <div class="rounded-xl overflow-hidden">
                                    <img src="/hero.png" alt="Jongisapho - Software Engineer"
                                    loading="lazy"
                                    class="w-[500px]. h-[500px] object-contain -translate-y-8">

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


</script>

<style>

</style>