<template>
    <section class="flex flex-col">
        <h1 class="bg-green-400 text-4xl p-4 text-center">{{ msg }}</h1>
        <button @click="count++">count is: {{ count }}</button>
        <p>
            Edit <code>components/HelloWorld.vue</code> to test hot module
            replacement.
        </p>
    </section>
</template>

<script>
export default {
    name: 'HelloWorld',
    props: {
        msg: String,
    },
    data() {
        return {
            count: 0,
        }
    },
}
</script>
