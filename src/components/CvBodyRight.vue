<template>
    <!-- Skills -->
    <div>
        <div class="text-4xl font-roboto font-black" id="right">Skills</div>
        <div>
            <h1 class="text-xl font-bold">Programing lamguages</h1>
            <ul
                v-for="(lang, index) in data.skills.programingLanguages"
                :key="index"
            >
                <li>{{ lang }}</li>
            </ul>
        </div>
        <div>
            <h1 class="text-xl font-bold">Libraries and Frameworks</h1>
            <ul
                v-for="(framework, index) in data.skills.LibrariesandFrameworks"
                :key="index"
            >
                <li>{{ framework }}</li>
            </ul>
        </div>
        <div>
            <h1 class="text-xl font-bold">Tools & Platforms</h1>
            <ul v-for="(plat, index) in data.skills.platforms" :key="index">
                <li>{{ plat }}</li>
            </ul>
        </div>
        <div>
            <h1 class="text-xl font-bold">Design</h1>
            <ul v-for="(design, index) in data.skills.Design" :key="index">
                <li>{{ design }}</li>
            </ul>
        </div>
        <!-- Education -->
        <div>
            <h1 class="text-xl font-bold">Education</h1>
            <ul v-for="(educ, index) in data.Education" :key="index">
                <li>
                    <span>{{ educ.place }}</span>
                    <span>{{ educ.startDate }}</span>
                    <span>{{ educ.endDate }}</span>
                    <span>{{ educ.location }}</span>
                    <p>{{ educ.description }}</p>
                </li>
            </ul>
        </div>
        <div>
            <h1 class="text-xl font-bold">Intrest</h1>
            <ul v-for="(intr, index) in data.Interests" :key="index">
                <li>
                    <span>{{ intr }}</span>
                </li>
            </ul>
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
