<template>
    <!-- Skills -->
    <div v-if="data.skills" class="ml-3">
        <div class="text-4xl font-roboto font-black" id="right">Skills</div>
        <div>
            <h1 class="text-xl font-bold">Programing lamguages</h1>
            <div
                v-for="(lang, index) in data.skills.programingLanguages"
                :key="index"
                class="inline-block"
            >
                <span class="mr-2">{{ lang }}</span>
            </div>
        </div>
        <div>
            <h1 class="text-xl font-bold">Libraries and Frameworks</h1>
            <div
                v-for="(framework, index) in data.skills.LibrariesFrameworks"
                :key="index"
                class="inline-block"
            >
                <div class="mr-2">{{ framework }}</div>
            </div>
        </div>
        <div>
            <h1 class="text-xl font-bold">Tools & Platforms</h1>
            <div
                v-for="(plat, index) in data.skills.platforms"
                :key="index"
                class="inline-block"
            >
                <div class="mr-2">{{ plat }}</div>
            </div>
        </div>
        <div>
            <h1 class="text-xl font-bold">Design</h1>
            <div
                v-for="(design, index) in data.skills.Design"
                :key="index"
                class="inline-block"
            >
                <div class="mr-2">{{ design }}</div>
            </div>
        </div>
        <!-- Education -->
        <div>
            <h1 class="text-xl font-bold">Education</h1>
            <div
                v-for="(educ, index) in data.Education"
                :key="index"
                class="inline-block"
            >
                <div class="mr-2">
                    <span class="font-bold mr-2">{{ educ.place }}</span>
                    <div class="inline-block">
                        <span class="mr-2">{{ educ.startDate }}</span>
                        <span>{{ educ.endDate }}</span>
                    </div>
                    <span>{{ educ.location }}</span>
                    <p>{{ educ.description }}</p>
                </div>
            </div>
        </div>
        <div>
            <h1 class="text-xl font-bold">Intrest</h1>
            <div
                v-for="(intr, index) in data.Interests"
                :key="index"
                class="inline-block"
            >
                <div class="mr-2">
                    <span>{{ intr }}</span>
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
