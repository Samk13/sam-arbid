<template>
    <!-- Skills -->
    <div v-if="data.skills" class="ml-3 space-y-4">
        <div class="text-3xl font-black" id="right">Skills</div>
        <div class="">
            <h1 class="text-xl font-bold text-gray-400 capitalize">
                Programing languages
            </h1>
            <div
                v-for="(lang, index) in data.skills.programingLanguages"
                :key="index"
                class="inline-block mt-2"
            >
                <span
                    class="mr-1 border rounded-lg px-2 py-1 text-xs capitalize"
                    >{{ lang }}</span
                >
            </div>
        </div>
        <div>
            <h1 class="text-xl font-bold text-gray-400 capitalize">
                Libraries and Frameworks
            </h1>
            <div
                v-for="(framework, index) in data.skills.LibrariesFrameworks"
                :key="index"
                class="inline-block mt-2"
            >
                <div
                    class="mr-1 border rounded-lg px-2 py-1 text-xs capitalize"
                >
                    {{ framework }}
                </div>
            </div>
        </div>
        <div>
            <h1 class="text-xl font-bold text-gray-400 capitalize">
                Tools & Platforms
            </h1>
            <div
                v-for="(plat, index) in data.skills.platforms"
                :key="index"
                class="inline-block mt-2"
            >
                <div
                    class="mr-1 border rounded-lg px-2 py-1 text-xs capitalize"
                >
                    {{ plat }}
                </div>
            </div>
        </div>
        <div>
            <h1 class="text-xl font-bold text-gray-400 capitalize">Design</h1>
            <div
                v-for="(design, index) in data.skills.Design"
                :key="index"
                class="inline-block mt-2"
            >
                <div
                    class="mr-1 border rounded-lg px-2 py-1 text-xs capitalize"
                >
                    {{ design }}
                </div>
            </div>
        </div>
        <!-- Education -->
        <div>
            <h1 class="text-3xl font-bold mb-2 capitalize">Education</h1>
            <div
                v-for="(educ, index) in data.Education"
                :key="index"
                class="inline-block"
            >
                <div class="mr-2">
                    <div class="font-bold block mb-0">{{ educ.place }}</div>
                    <div>
                        <div class="mb-2 text-gray-500 text-xs">
                            {{ educ.startDate }} - {{ educ.endDate }} /
                            {{ educ.location }}
                        </div>
                    </div>
                    <p class="text-xs mb-3">{{ educ.description }}</p>
                </div>
            </div>
        </div>
        <div>
            <h1 class="text-3xl font-bold mb-2 capitalize">Intrest</h1>
            <div
                v-for="(intr, index) in data.Interests"
                :key="index"
                class="inline-block"
            >
                <div class="mr-2 mt-2">
                    <span class="mr-1 border rounded-lg px-2 py-1 text-xs">{{
                        intr
                    }}</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CvBodyRight',
    props: {
        data: {
            type: Object,
            required: true,
        },
    },
}
</script>
