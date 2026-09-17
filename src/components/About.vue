<<template>
    <section class="bg-slate-950 relative py-20 overflow-hidden min-h-screen flex items-center" id="about">
        <div class="w-full px-5 sm:px-8 md:px-12 lg:px-5 max-w-5xl lg:max-w-7xl mx-auto relative z-10">
            <div class="flex items-center justify-center">
                <div class="lg:h-full flex justify-center lg:justify-start order-2 lg:order-1">
                    <div class="relative w-full max-w-md">
                        <div class="flex group items-center gap-2 flex-col sm:flex-row sm:w-max sm:mx-auto mt-10 md:items-center md:ml-20 lg:ml-12"
                            data-aos="fade-up" data-aos-delay="300">
                        </div>
                    </div>
                </div>

                <div class="w-full max-w-4xl text-center" data-aos="fade-left">
                    <h2 class="text-white font-bold text-4xl md:text-5xl lg:text-6xl leading-tight">
                        About <span class="text-transparent bg-clip-text bg-linear-to-r bg-blue-500">
                            Me</span>
                    </h2>
                    <p class="text-white font-extrabold pt-4">
                        BSc Honours Computer Science Student
                    </p>
                    <p class="text-white pt-2 text-center text-lg leading-relaxed" data-aos="fade-left"
                        data-aos-delay="200">
                        I build thoughtful, reliable software across full-stack development, natural language
                        processing and data analytics. My work focuses on maintainable systems that solve real-world
                        problems and create clear digital experiences.
                    </p>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 pt-6 pb-4 " data-aos="fade-up"
                        data-aos-delay="300">
                        <div v-for="skill in skills" :key="skill.id" class="flex flex-col">
                            <div class="flex items-center justify-center gap-3 mb-3">
                                <component :is="skill.icon" class="w-6 h-6 lg:w-10 lg:h-10 hover:scale-200"
                                    :class="skill.iconColor">

                                </component>
                                <h3 class="text-lg font-bold text-white">
                                    {{ skill.title }}
                                </h3>
                            </div>
                            <p class="text-white text-sm font-bold ">
                                {{ skill.desc }}
                            </p>
                        </div>

                    </div>
                </div>
            </div>



        </div>
    </section>
</template>

    <script setup>

    import { ArrowRightIcon, ChatBubbleLeftRightIcon, CodeBracketSquareIcon, CubeIcon, PaintBrushIcon, ServerIcon } from '@heroicons/vue/16/solid';
    import about1 from '../assets/about1.png';
    import about2 from '../assets/about2.png';
    import about3 from '../assets/about3.png';
    import about4 from '../assets/about4.png';

    const aboutImage = [
        {
            id: 1,
            src: about1,
            alt: "Jongi - Professional Photo",
            gradient: `bg-linear-to-r from-blue-600 to-cyan-600 border-blue-400/40`,
            badge: 'Professional',
            badgeColor: 'bg-blue-500',
            animation: 'fade-right',
            delay: 200

        },
        {
            id: 2,
            src: about2,
            alt: "Jongi - Working Environment",
            gradient: `bg-linear-to-r from-blue-500 to-cyan-500 border-blue-400/40`,
            badge: 'Creative',
            badgeColor: 'bg-cyan-500',
            animation: 'fade-left',
            delay: 300

        },
        {
            id: 3,
            src: about3,
            alt: "Jongi - Professional Photo",
            gradient: `bg-linear-to-r from-blue-500 to-cyan-500 border-blue-400/40`,
            badge: 'Developer',
            badgeColor: 'bg-blue-600',
            animation: 'fade-right',
            delay: 400

        },
        {
            id: 4,
            src: about4,
            alt: "Jongi - Design Work",
            gradient: `bg-linear-to-r from-blue-600 to-cyan-600 border-blue-400/40`,
            badge: 'Designer',
            badgeColor: 'bg-cyan-600',
            animation: 'fade-left',
            delay: 500

        },
    ]

    const skills = [
        {
            id: 1,
            icon: CodeBracketSquareIcon,
            iconColor: "text-red-400",
            title: 'Frontend',
                            desc: "React, Vue.js, JavaScript, HTML, CSS, Tailwind CSS, Vite"
        },
        {
            id: 2,
            icon: ServerIcon,
            iconColor: "text-green-400",
            title: 'Backend',
                            desc: "Node.js, Express.js, SQLite, PostgreSQL, MySQL, MongoDB"
        },
        {
            id: 3,
            icon: PaintBrushIcon,
            iconColor: "text-blue-400",
            title: 'Design',
                            desc: "Figma, Canva, responsive design and prototyping"
        },
        {
            id: 4,
            icon: CubeIcon,
            iconColor: "text-cyan-400",
            title: 'Tools',
                            desc: "Git, GitHub, Docker, Postman, Power BI and Jest"
        },
    ]

    const ctaButtons = [
        {
            id: 1,
            text: 'View Portfolio',
            icon: ArrowRightIcon,
            iconclass: `ml-2 group-hover:translate-x-1 transition-transform`,
            classes: `bg-linear-to-r from-blue-600 to-cyan-600 text-white hover:from-blue-500 hover:to-cyan-500`
        },
        {
            id: 2,
            text: 'Contact Me',
            icon: ChatBubbleLeftRightIcon,
            iconclass: `mr-2`,
            classes: `border border-blue-400 text-blue-400`
        },

    ]
</script>
