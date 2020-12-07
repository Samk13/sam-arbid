<template>
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
</template>

<script>
export default {
    name: 'CvBodyLeft',
    props: {
        data: {
            type: Object,
            required: true,
        },
    },
}
</script>
