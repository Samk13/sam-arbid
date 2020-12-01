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
        <div class="font-roboto font-black" id="left">
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
        </div>
        <div class="text-4xl font-roboto font-black" id="right">Skills</div>
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
