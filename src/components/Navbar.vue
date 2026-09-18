<template>
    <header class="relative z-20 bg-slate-950/95">
        <div class="flex min-h-20 w-full max-w-7xl mx-auto items-center justify-between px-5 sm:px-8 md:px-12 lg:px-5">
            <a href="#about" @click="scrollToSection('#about')"
                class="min-w-44 text-3xl transition-all duration-500 hover:text-blue-500 font-bold bg-white bg-clip-text text-transparent">
                <span v-if="showWelcome">Welcome</span>
                <span v-else>My<span class="font-black"> Portfolio </span></span>
            </a>

            <div class="md:hidden z-30">
                <button type="button" class="group block focus:outline-none p-2.5 border-2 border-blue-500 hover:border-white rounded-lg bg-black
                hover:bg-blue-500 transition-all duration-300" @click="isMenuOpen = !isMenuOpen">
                    <div class="relative w-6 h-6">
                        <span :class="[
                            'absolute left-0 w-6 h-0.5 bg-blue-500 transition-all duration-300 group-hover:bg-white',
                            isMenuOpen ? 'rotate-45 top-3' : 'top-1'
                        ]"></span>
                        <span :class="[
                            'absolute left-0 w-6 h-0.5 bg-blue-500 transition-all duration-300 group-hover:bg-white',
                            isMenuOpen ? 'opacity-0' : 'top-3 opacity-100'
                        ]"></span>
                        <span :class="[
                            'absolute left-0 w-6 h-0.5 bg-blue-500 transition-all duration-300 group-hover:bg-white',
                            isMenuOpen ? '-rotate-45 top-3' : 'top-5'
                        ]"></span>
                    </div>
                </button>
            </div>

            <nav :class="[
                'fixed inset-0 z-20 flex flex-col items-center justify-center bg-slate-950 md:relative md:bg-transparent md:flex md:justify-between md:flex-row transition-all duration-200 transform',
                isMenuOpen ? 'opacity-100 translate-y-0 pointer-events-auto delay-300'
                    : 'opacity-0 -translate-y-4 pointer-events-none md:opacity-100 md:translate-y-0 md:pointer-events-auto'
            ]">
                <ul class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0">
                    <li v-for="item in Menu" :key="item.name" class="group relative">
                        <a :href="item.href" class="relative inline-block text-blue-100 group-hover:text-blue-500 transition-all duration-300 text-xl md:text-white md:text-base font-medium"
                            @click="scrollToSection(item.href)">
                            {{ item.name }}
                            <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-blue-500 transition-all duration-500 group-hover:w-full"></span>
                        </a>
                    </li>
                </ul>
                <div class="mt-6 md:mt-0 md:ml-7 group">
                    <a href="#contact" @click.prevent="openContactModal" class="px-5 py-2.5 rounded-lg border-2 border-blue-500 text-blue-500 text-sm font-semibold hover:bg-blue-400/10 transition-all duration-300 flex items-center text-nowrap">
                        Let's Talk
                    </a>
                </div>
            </nav>
        </div>
    </header>
</template>

<script setup>
import { onMounted, onUnmounted, ref } from 'vue';

const Menu = ref([
    { name: 'Services', href: '#services' },
    { name: 'About Me', href: '#about' },
    { name: 'Skills', href: '#skills' },
]);

const isMenuOpen = ref(false);
const showWelcome = ref(true);
let welcomeTimer;

onMounted(() => {
    welcomeTimer = window.setTimeout(() => {
        showWelcome.value = false;
    }, 3000);
});

onUnmounted(() => {
    window.clearTimeout(welcomeTimer);
});

const scrollToSection = (href) => {
    isMenuOpen.value = false;
    const section = document.querySelector(href);
    if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
    }
}

const openContactModal = () => {
    isMenuOpen.value = false;
    window.dispatchEvent(new Event('open-contact-modal'));
};
</script>
