<template>
    <button
        :class="[
            'px-8 md:px-10 md:py-2 py-3 roundedd-full relative group w-full sm:w-max flex justify-center overflow-hidden transition-all duration-300 hover:scale-105',
            variant === 'primary' ? 'bg-linear-to-r from-blue-400 via-red-200 to-cyan-600' : '',
            variant === 'secondary' ? 'bg-linear-to-r from-cyan-400 via-red-200 to-blue-600': '',
            variant === 'nav' ? 'bg-linear-to-r from-blue-400 via-red-200 to-cyan-600': '',
            customClass 
        ]"
        @click="handleClick"
    >
        <span class="relative flex items-center justify-center text-white font-semibold text-lg">
            <slot name="icon-left"></slot>
            {{ label }}
            <slot name="icon-right"></slot>
        </span>
    </button>
</template>

<script setup>
const props = defineProps({
    label: {
        type: String,
        default: 'Button'
    },
    variant: {
        type: String,
        default: 'primary',
        validator: (value) => ['primary', 'secondary', 'nav'].includes(value)
    },
    customClass: {
        type: String,
        default: ''
    }
});

const emit = defineEmits(['click']);

const handleClick = (event) => {
    emit('click', event);
};
</script>