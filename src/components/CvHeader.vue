<template>
    <div class="py-5">
        <div class="mb-5">
            <h1 class="text-5xl font-black text-green-400">
                {{ data.name }}
            </h1>
            <hr class="border-1" />
            <h2 class="text-gray-500 font-black text-md animate-pulse">
                {{ data.title }}
            </h2>
        </div>
        <div>
            <ul class="-space-y-1">
                <li>{{ data.address }}</li>
                <li>{{ data.email }}</li>
                <li>{{ data.github }}</li>
                <li>{{ data.mobile }}</li>
            </ul>
        </div>
    </div>
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
