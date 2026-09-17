<template>
    <section class="relative w-full overflow-hidden min-h-screen flex items-center bg-slate-950">
        <div class="text-white w-full max-w-5xl lg:max-w-7xl mx-auto relative z-10 px-5 sm:px-8 lg:px-5">
            <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
                <div class="flex min-w-0 flex-col justify-center lg:-mt-40 mt-5">
                    <div class="text-white text-center" data-aos="fade-right">
                        <h1 class="font-bold text-4xl sm:text-5xl md:text-4xl">
                            Hello, I'm
                            <span class="text-transparent bg-clip-text bg-linear-to-r bg-blue-500 ">Jongisapho
                                Ndeya</span>

                        </h1>
                        <p class="font-medium text-lg sm:text-xl mt-5" data-aos="fade-right" data-aos-delay="500">
                            Software Developer | NLP Researcher | Data Analyst
                        </p>
                    </div>
                    <p class="text-gray-200 text-center mx-auto max-w-xl text-base sm:text-lg leading-relaxed mt-8 sm:mt-10">
                        I am a BSc Honours Computer Science student focused on software development, natural language
                        processing and data analytics. I build scalable full-stack applications and enjoy solving real
                        problems with focus, speed and enthusiasm.
                    </p>
                    <div class="flex group items-center  gap-4 flex-col sm:flex-row sm:w-max sm:mx-auto mt-10"
                        data-aos="fade-up" data-aos-delay="300">
                        <a href="#about" class="px-5 py-2.5 rounded-lg border-2 border-blue-500 text-blue-500 text-sm font-semibold
            hover:bg-blue-400/10 transition-all duration-300 flex items-center text-nowrap">
                            Lets Talk
                            <ArrowRightIcon class="w-5 h-5 ml-2" />
                        </a>
                        <a href="#skills" class="px-5 py-2.5 rounded-lg border-2 border-blue-500 text-blue-500 text-sm font-semibold
            hover:bg-blue-400/10 transition-all duration-300 flex items-center">
                            View Skills
                            <ArrowDownTrayIcon class="w-5 h-5 ml-2" />
                        </a>
                    </div>
                </div>
                <div class="flex items-center justify-center lg:justify-start gap-8 md:ml-30 pt-4" data-aos="fade-up"
                    data-aos-delay="400">
                    <div class="lg:h-full flex justify-center lg:justify-end">
                        <div class="relative w-full max-w-md lg:max-w-lg">
                            <div class="relative z-10 bg-linear-to-r from-blue-400  shadow-3xl rounded-[50%_40%_40%_60%/60%_30%_50%_30%]
                            p-4 backdrop-blur-sm border border-blue-500/10
                            -translate-y-6" data-aos="zoom-in" data-aos-delay="500">
                                <div class="rounded-xl overflow-hidden">
                                    <img src="../assets/public/hero.png" alt="Jongisapho - Software Engineer"
                                        loading="lazy" class="w-[500px]. h-125 object-contain -translate-y-8">

                                </div>
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

<style></style>