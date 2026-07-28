<<template>
    <section class="bg-slate-950 relative py-20 overflow-hidden min-h-screen flex items-center" id="about">
        <div class="w-full px-5 sm:px-8 md:px-12 lg:px-5 max-w-5xl lg:max-w-7xl mx-auto relative z-10">
            <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
                <div class="lg:h-full flex justify-center lg:justify-start order-2 lg:order-1">
                    <div class="relative w-full max-w-md">
                        <div class="relative md:-right-10  bg-slate-950 ">
                            <div class="grid grid-cols-2 gap-2">
                                <div v-for="(image, index) in aboutImage" :key="image.id" class="relative group"
                                    :data-aos="image.animation" :data-aos-delay="image.delay">
                                    <div class="rounded-3xl  shadow-lg " :class="image.gradient">
                                        <img :src="image.src" :alt="image.alt"
                                            class="w-full h-48 object-cover bg-blue-400 rounded-xl group-hover:scale-105 transition-trransform duration-300">


                                    </div>
                                    <div class="absolute -top-2 -right-2 text-white text-xs px-2 py-1 rounded-full font-semibold"
                                        :class="image.badgeColor">
                                        {{ image.badge }}
                                    </div>
                                </div>
                            </div>
                            <div class="absolute -bottom-4 left-1/2 transform translate-x-1/2 z-20 bg-slate-950 rounded-2xl px-6 py-3 border-2 border-blue-500 shadow-xl"
                                data-aos="fade-up" data-aos-delay="600">
                                <div class="text-center text-blue-500 text-xl font-bold"> 3+ Years Experience</div>
                            </div>
                        </div>
                        <div class="flex group items-center gap-2 flex-col sm:flex-row sm:w-max sm:mx-auto mt-10 md:items-center md:ml-20 lg:ml-12"
                            data-aos="fade-up" data-aos-delay="300">
                            <button class="px-8 py-4 rounded-2xl border-2 border-blue-500 text-blue-500 font-semibold
            hover:bg-blue-400/10 transition-all duration-300 flex items-center text-nowrap">
                                View Portfolio
                                <ArrowRightIcon class="w-6 h-6 ml-2" />
                            </button>
                            <button class="px-10 py-4 rounded-2xl border-2 border-blue-500 text-blue-500 font-semibold
            hover:bg-blue-400/10 transition-all duration-300 flex items-center text-nowrap">
                                Contact Me
                                <ChatBubbleLeftRightIcon class="w-6 h-6 ml-2" />

                            </button>
                        </div>
                    </div>
                </div>

                <div class="text-center lg:text-left" data-aos="fade-left">
                    <h2 class="text-white font-bold text-4xl md:text-5xl lg:text-6xl leading-tight">
                        About <span class="text-transparent bg-clip-text bg-linear-to-r bg-blue-500">
                            Me</span>
                    </h2>
                    <p class="text-white font-extrabold pt-4">
                        Software Developer & ML Engineering student
                    </p>
                    <p class="text-white pt-2 text-center lg:text-left text-lg leading-relaxed" data-aos="fade-left"
                        data-aos-delay="200">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
                        labore
                        et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi
                        ut
                        aliquip ex ea commodo consequat.
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
            desc: "Vue js, React, JavaScript, TypeScript, TailwindCSS"
        },
        {
            id: 2,
            icon: ServerIcon,
            iconColor: "text-green-400",
            title: 'Backend',
            desc: "Node js, Express, MongoDB, SQL, REST APIs, Postgres, SQLite"
        },
        {
            id: 3,
            icon: PaintBrushIcon,
            iconColor: "text-blue-400",
            title: 'Design',
            desc: "UI/UX Design, Figma, Responsive Design, Prototyping"
        },
        {
            id: 4,
            icon: CubeIcon,
            iconColor: "text-cyan-400",
            title: 'Tools',
            desc: "Git, Docker, VSCode, NPM, JWT, Git, Github, Postman, Docker, Jest"
        },
    ]

    const ctaButtons = [
        {
            id: 1,
            text: 'View Portfolio',
            icon: ArrowRightIcon,
            iconclass: `ml-2 group-hover: translate-x-1 tranisition-transform`,
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
