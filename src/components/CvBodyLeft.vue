<template>
    <section class="w-1/3" id="left">
        <h1 class="font-black text-4xl">Relevant Experience</h1>
        <div v-for="xp in data" :key="xp.id">
            <div id="capcito">
                <h2 class="text-xl font-bold">
                    <span>{{ xp.title }} @ {{ xp.place }}</span>
                </h2>
                <h2 class="text-gray-500 text-xs">
                    <span>{{ xp.startDate }} - {{ xp.endDate }}</span>
                </h2>
                <ul
                    v-for="(desc, index) in xp.description"
                    :key="index"
                    class="my-3 text-xs"
                >
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
