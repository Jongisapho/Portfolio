<<template>
    <section class="relative py-20 overflow-hidden bg-slate-950" id="skills">
        <div class="relative z-10 max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 text-white" data-aos="fade-up">
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                    Skills &
                    <span class="text-transparent bg-clip-text bg-blue-500">
                        Experience
                    </span>
                </h2>
                <p class="text-white text-lg max-w-2xl mx-auto">
                    My technical expertise and professional journey
                </p>
            </div>
            <div class="grid lg:grid-cols-2 gap-12 lg:gap-16">
                <div data-aos="fade-right">
                    <h3 class="text-2xl font-bold text-white mb-8 flex items-center gap-3">
                        Technical skills
                    </h3>
                    <div class="space-y-6">
                        <div v-for="skill in skills" :key="skill.id" class="group">
                            <div class="flex items-center justify-between mb-3">
                                <span class="text-blue-200 font-semibold flex items-center gap-2">
                                    <component :is="skill.icon" class="w-5 h-5" :class="skill.iconColor"></component>
                                    {{ skill.title }}
                                </span>
                                <span :class="skill.percentageColor">
                                    {{ skill.percentage }} %
                                </span>
                            </div>
                            <div class="h-3 bg-gray-700 rounded-full overflow-hidden">
                                <div class="h-full rounded-full transition-all duration-1000 group-hover:scale-105"
                                    :class="skill.gradient" :style="{ width: skill.percentage + '%' }">

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

    import { CodeBracketIcon, ServerIcon, PaintBrushIcon, DevicePhoneMobileIcon, SparklesIcon } from '@heroicons/vue/16/solid';
    const skills = [
        {
            id: 1,
            title: "Frontend Development",
            icon: CodeBracketIcon,
            iconColor: 'text-cyan-400',
            percentage: 90,
            percentageColor: "text-blue-400 text-sm",
            gradient: 'bg-linear-to-r from-blue-500 to-cyan-500'
        },
        {
            id: 2,
            title: "Backend Development",
            icon: ServerIcon,
            iconColor: 'text-blue-400',
            percentage: 90,
            percentageColor: "text-cyan-400 text-sm",
            gradient: 'bg-linear-to-r from-cyan-500 to-blue-500'
        },
        {
            id: 3,
            title: "UI/UX Design",
            icon: PaintBrushIcon,
            iconColor: 'text-cyan-400',
            percentage: 90,
            percentageColor: "text-blue-400 text-sm",
            gradient: 'bg-linear-to-r from-blue-500 to-cyan-500'
        },
        {
            id: 4,
            title: "Mobile Development",
            icon: DevicePhoneMobileIcon,
            iconColor: 'text-blue-400',
            percentage: 90,
            percentageColor: "text-cyan-400 text-sm",
            gradient: 'bg-linear-to-r from-cyan-500 to-blue-500'
        },
        {
            id: 5,
            title: "AI & ML Engineering",
            icon: SparklesIcon,
            iconColor: 'text-cyan-400',
            percentage: 20,
            percentageColor: "text-blue-500 text-sm",
            gradient: 'bg-linear-to-r from-blue-500 to-cyan-500'
        }
    ]

    const experiences = [
        {
            id: 1,
            position: "Intern Data Scientist",
            company: "Telkom.",
            period: "2023 Januanry",
            desc: "Lorem ipsum dolot sit amet consectetur adispicing elit.Q",
            borderColor: "border-blue-500/50",
            dotColor: "bg-blue-500",
            borderClass: "border-blue-500/20",
            dateColor: "text-blue-400 text-sm fonr-semibold",
            companyColor: "text-cyan-400"
        }
    ]

    const techStack = [
        'Vue Js', 'React', 'JavaScript', 'TypeScript', 'Java', 'C++', 'Node js', 'Express', 'TailwindCSS',
        'MongoDB', 'Postgres', 'SQL', 'Docker', 'VScode', 'Python', 'REST APIs', 'Git',
        'Github', 'Postman', 'Jest', 'Figma'
    ]

</script>