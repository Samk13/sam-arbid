<template>
    <section class="container m-auto flex flex-col">
        <div class="ml-4">
            <h1 class="text-5xl font-black text-green-500">
                {{ data.name }}
            </h1>
            <hr class="border-2" />
            <h2>{{ data.title }}</h2>
        </div>
        <div>
            <ul>
                <li>{{ data.address }}</li>
                <li>{{ data.email }}</li>
                <li>{{ data.github }}</li>
                <li>{{ data.mobile }}</li>
            </ul>
        </div>
    </section>
    <section class="flex w-full justify-between">
        <section class="font-roboto font-black w-1/3" id="left">
            <h1>Relevant Experience</h1>
            <div v-for="xp in data.relevantExperience" :key="xp.id">
                <div id="capcito">
                    <h2>
                        <span>{{ xp.title }} @ {{ xp.place }}</span>
                    </h2>
                    <h2>
                        <span>{{ xp.startDate }} - {{ xp.endDate }}</span>
                    </h2>
                    <ul v-for="(desc, index) in xp.description" :key="index">
                        <li>
                            {{ desc }}
                        </li>
                    </ul>
                </div>
            </div>
        </section>
        <!-- Skills -->
        <div class="w-1/3">
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
                    v-for="(framework, index) in data.skills
                        .LibrariesandFrameworks"
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
    </section>
</template>

<script>
export default {
    name: 'CvHeader',
    props: {
        data: {
            type: Object,
            required: true,
        },
    },
}
</script>
