<template>
    <section class="relative overflow-hidden bg-slate-950" id="services">
        <div class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 lg:px-1">
            <div class="text-center m-16" data-aos="fade-up">
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                    My <span
                        class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 via-red-200 to-cyan-600">Services</span>
                </h2>
                <p class="text-white text-lg max-w-2xl mx-auto" data-aos="fade-up" data-aos-delay="100">
                    This is a list of services that I offer, Please note that this list is not limited and is subject to
                    change with time .
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div v-for="(service, index) in services" :key="service.id" data-aos="fade-up"
                    :data-aos-delay="(index * 100) + 200"
                    class="group relative p-8 rounded-2xl bg-linear-to-br from-gray-800/50 via-cyan-300/10 to-blue-900/30 backdrop-blur-sm border border-blue-500/20 hover:border-blue-400/40 transition-all duration-500 hover:transform hover:-translate-y-2">
                    <div
                        class="absolute inset-0 bg-linear-to-r from-blue-500/6 to-cyan-500/4 rounded-2xl opacity-0 duration-500 group-hover:opacity-100 transition-opacity">
                    </div>
                    <div class="relative z-10 mb-6">
                        <div class="inline-flex items-center justify-center
              w-16 h-16 rounded-xl bg-linear-to-r from-blue-500/20 to-cyan-500/20 border border-blue-400/30
              group-hover:scale-110 transition-transform duration-300">
                            <component :is="service.icon" class="w-8 h-8 text-blue-400">
                            </component>
                        </div>
                    </div>
                    <div class="relative z-10">
                        <h3
                            class="text-xl font-bold text-white mb-3 group-hover:text-blue-400 transition-colors duration-300">
                            {{ service.name }}
                        </h3>
                        <p class="text-white">
                            {{ service.desc }}
                        </p>
                    </div>
                    <div
                        class="absolute bottom-6 right-6 opacity-0 group-hover:opacity-100 transform translate-x-4 group-hover:translate-x-0 transition-all duration-300">
                        <ArrowRightIcon class="w-6 h-6 text-cyan-300" />
                    </div>
                </div>
            </div>

            <div class="text-center mt-16" data-aos="fade-up" data-aos-delay="800">
                <div class="inline-flex flex-col sm:flex-row gap-4 items-center">
                    <button class="px-8 py-4 rounded-xl border-2 border-blue-400 text-blue-400 font-semibold
            hover:bg-blue-400/10 transition-all duration-300 flex items-center">
                        Get In Touch
                        <ChatBubbleLeftRightIcon class="w-5 h-5 ml-2" />
                    </button>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';
import {
    CodeBracketIcon,
    DocumentTextIcon,
    DevicePhoneMobileIcon,
    EnvelopeIcon,
    PaintBrushIcon,
    ComputerDesktopIcon,
    ChatBubbleLeftRightIcon,
    ArrowRightIcon
} from '@heroicons/vue/16/solid';

const services = ref([
    {
        id: 1,
        icon: CodeBracketIcon,
        name: 'Software Development',
        desc: 'Developing robust software solutions tailored to your daily business needs.'
    },
    {
        id: 2,
        icon: DevicePhoneMobileIcon,
        name: 'Web Development',
        desc: 'Developing modern, responsive and secure web applications using cutting-edge technologies.'
    },
    {
        id: 3,
        icon: ComputerDesktopIcon,
        name: 'AI & Machine Learning',
        desc: 'Implementing intelligent algorithms and automated systems to solve complex business challenges.'
    },
    {
        id: 4,
        icon: PaintBrushIcon,
        name: 'UI/UX Design',
        desc: 'Designing intuitive and beautiful user interfaces with focus on user experience.'
    },
    {
        id: 5,
        icon: DocumentTextIcon,
        name: 'IT Consulting',
        desc: 'Providing expert IT consulting to help you make informed technology decisions.'
    },
    {
        id: 6,
        icon: EnvelopeIcon,
        name: 'Email Automation',
        desc: 'Implementing email automation systems for better customer engagement.'
    },
    
]);
</script>

<style></style>