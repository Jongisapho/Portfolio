<template>
    <header class="flex justify-between p-6 bg-opacity-50 bg-slate-950 relative z-20">
        <div class="text-3xl font-bold bg-white bg-clip-text text-transparent">
            Dev <span class="font-black"> Portfolio </span>
        </div>
        <div class="md:hidden z-30 ">
            <button type="button" class="group block focus:outline-none p-2 rounded-lg bg-white
                hover:bg-blue-400 transition-all duration-300" @click="isMenuOpen = !isMenuOpen">
                <div class="relative w-6 h-6">
                    <span :class="[
                        `absolute left-0 w-6 h-0.5 bg-slate-800 transition-all
                        duration-400 group-hover:bg-white`,
                        isMenuOpen ? 'rotate-45 top-3 ' : 'top-1'
                    ]">
                    </span>
                    <span :class="[
                        `absolute left-0 w-6 h-0.5 bg-slate-800 transition-all
                        duration-400 group-hover:bg-white`,
                        isMenuOpen ? 'opacity-0' : 'top-3 opacity-100'
                    ]">
                    </span>
                    <span :class="[
                        `absolute left-0 w-6 h-0.5 bg-slate-800 transition-all
                        duration-400 group-hover:bg-white`,
                        isMenuOpen ? '-rotate-45 top-3 ' : 'top-5'
                    ]">
                    </span>
                </div>
            </button>
        </div>
        <nav :class="[
            `fixed inset-0 z-20 flex flex-col items-center justify-center bg-slate-950 md:relative md:bg-transparent md:flex
            md-justify-between md:flex-row` ,
            isMenuOpen ? 'block' : 'hidden'
        ]">
            <ul class="flex flex-col items-center space-y-5 md:flex-row
            md:space-x-5 md:space-y-0">
                <li v-for="item in Menu" :key="item.name" class="group relative">
                    <a :href="item.href"
                    class="relative block text-blue-100 hover:text-blue-300
                    transition-all duration-300 text-xl md:text-white md:text-base font-medium
                    group"
                    @click="scrollToSection(item.href)">
                    {{ item.name }}
                    <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-blue-400
                    transition-all duration-500 group-hover:w-full">
                    
                    </span>
                    </a>
                </li>
            </ul>
            <div class="mt-6 md:mt-0 md:ml-7 ">
                <button class="px-6 py-2.5 bg-linear-to-r from-blue-500 to-cyan-500 text-white rounded-full hover:shadow-lg hover:shadow-blue-500/25 transition-all duration-300 hover:scale-105">
                    Let's Talk
                </button>
            </div>

        </nav>
    </header>
</template>

<script setup>
import { ref } from 'vue';

const Menu = ref([
    { name: 'Services', href: '#services' },
    { name: 'About Me', href: '#about' },
    { name: 'Skills', href: '#skills' },
    { name: 'Projects', href: '#projects' },
    { name: 'Testimonials', href: '#testimonials' },
    { name: 'Contacts', href: '#contacts' },
]);
const isMenuOpen = ref(false);
const scrollToSection = (href) => { // fat arrow function
    isMenuOpen.value = false; //automatically close Menu
    if (section) {
        section.scrollInview({ behavior: 'smooth' });
    }
}

</script>