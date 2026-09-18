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
                            Software Developer | Machine Learning & AI Enthusiast | Computer Science Researcher
                        </p>
                    </div>
                    <p class="text-gray-200 text-center mx-auto max-w-xl text-base sm:text-lg leading-relaxed mt-8 sm:mt-10">
                        I am a BSc Honours Computer Science student at the University of Pretoria, curious about how
                        intelligent systems understand, interpret and assist people. I build software, explore AI and
                        keep asking better questions about what technology can do in the real world.
                    </p>
                    <div class="flex group items-center  gap-4 flex-col sm:flex-row sm:w-max sm:mx-auto mt-10"
                        data-aos="fade-up" data-aos-delay="300">
                        <button type="button" @click="openModal('contact')" class="px-5 py-2.5 rounded-lg border-2 border-blue-500 text-blue-500 text-sm font-semibold
            hover:bg-blue-400/10 transition-all duration-300 flex items-center text-nowrap">
                            Lets Talk
                            <ArrowRightIcon class="w-5 h-5 ml-2" />
                        </button>
                        <button type="button" @click="openModal('skills')" class="px-5 py-2.5 rounded-lg border-2 border-blue-500 text-blue-500 text-sm font-semibold
            hover:bg-blue-400/10 transition-all duration-300 flex items-center">
                            View Skills
                            <ArrowDownTrayIcon class="w-5 h-5 ml-2" />
                        </button>
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

        <Transition name="modal">
            <div v-if="activeModal" class="fixed inset-0 z-50 flex items-center justify-center bg-slate-950/80 px-5 backdrop-blur-sm"
                @click.self="closeModal" role="presentation">
                <section class="relative w-full max-w-lg overflow-hidden rounded-2xl border border-blue-400/30 bg-slate-900 p-6 text-white shadow-2xl shadow-blue-950/50 sm:p-8"
                    role="dialog" aria-modal="true" :aria-labelledby="`${activeModal}-modal-title`">
                    <button type="button" @click="closeModal" aria-label="Close dialog"
                        class="absolute right-4 top-4 flex h-9 w-9 items-center justify-center rounded-full border border-white/20 text-xl text-gray-300 transition hover:border-blue-400 hover:text-white">
                        <span aria-hidden="true">&times;</span>
                    </button>

                    <div v-if="activeModal === 'contact'">
                        <p class="text-sm font-semibold uppercase tracking-[0.25em] text-cyan-300">Open channel</p>
                        <h2 id="contact-modal-title" class="mt-3 text-3xl font-bold">Let's Talk.</h2>
                        <p class="mt-3 text-gray-300">Reach out through which ever channel suits you best.</p>
                        <div class="mt-7 grid gap-3">
                            <a href="tel:+27707587825" class="rounded-xl border border-white/10 bg-white/5 px-4 py-3 transition hover:border-blue-400/60 hover:bg-blue-500/10">
                                <span class="block text-xs uppercase tracking-wider text-gray-400">Phone</span>
                                <span class="mt-1 block font-medium">+27 70 758 7825</span>
                            </a>
                            <a href="mailto:Jongisaphondeya1@gmail.com" class="rounded-xl border border-white/10 bg-white/5 px-4 py-3 transition hover:border-blue-400/60 hover:bg-blue-500/10">
                                <span class="block text-xs uppercase tracking-wider text-gray-400">Email</span>
                                <span class="mt-1 block break-all font-medium">Jongisaphondeya1@gmail.com</span>
                            </a>
                            <a href="https://linkedin.com/in/jongisapho-ndeya" target="_blank" rel="noreferrer" class="rounded-xl border border-white/10 bg-white/5 px-4 py-3 transition hover:border-blue-400/60 hover:bg-blue-500/10">
                                <span class="block text-xs uppercase tracking-wider text-gray-400">LinkedIn</span>
                                <span class="mt-1 block break-all font-medium">linkedin.com/in/jongisapho-ndeya</span>
                            </a>
                            <a href="https://jongisapho.versel.app" target="_blank" rel="noreferrer" class="rounded-xl border border-cyan-400/30 bg-cyan-400/10 px-4 py-3 transition hover:border-cyan-300 hover:bg-cyan-400/20">
                                <span class="block text-xs uppercase tracking-wider text-cyan-200">Website</span>
                                <span class="mt-1 block break-all font-medium">Jongisapho.vercel.app</span>
                            </a>
                        </div>
                    </div>

                    <div v-else>
                        <p class="text-sm font-semibold uppercase tracking-[0.25em] text-cyan-300">Choose your route</p>
                        <h2 id="skills-modal-title" class="mt-3 text-3xl font-bold">How would you like to explore?</h2>
                        <p class="mt-3 text-gray-300">Take the quick route through my CV or browse the skills section below.</p>
                        <div class="mt-7 grid gap-3 sm:grid-cols-2">
                            <a href="/Jongisapho-Ndeya-CV.pdf" download class="rounded-xl bg-blue-500 px-4 py-4 text-center font-semibold text-white transition hover:bg-blue-400">
                                Download CV
                                <span class="mt-1 block text-xs font-normal text-blue-100">PDF format</span>
                            </a>
                            <a href="#skills" @click="closeModal" class="rounded-xl border border-white/20 px-4 py-4 text-center font-semibold transition hover:border-cyan-300 hover:bg-cyan-400/10">
                                Scroll to skills
                                <span class="mt-1 block text-xs font-normal text-gray-300">See my toolkit</span>
                            </a>
                        </div>
                    </div>
                </section>
            </div>
        </Transition>

    </section>
</template>

<script setup>

import { onMounted, onUnmounted, ref } from 'vue';
import { ArrowRightIcon, ArrowDownTrayIcon } from '@heroicons/vue/16/solid';

const activeModal = ref(null);

const openModal = (modal) => {
    activeModal.value = modal;
};

const closeModal = () => {
    activeModal.value = null;
};

const handleKeydown = (event) => {
    if (event.key === 'Escape') closeModal();
};

onMounted(() => window.addEventListener('keydown', handleKeydown));
onUnmounted(() => window.removeEventListener('keydown', handleKeydown));

</script>

<style>
.modal-enter-active,
.modal-leave-active {
    transition: opacity 0.2s ease;
}

.modal-enter-from,
.modal-leave-to {
    opacity: 0;
}
</style>