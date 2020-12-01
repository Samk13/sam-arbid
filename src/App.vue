<template>
    <section>
        <!-- <HelloWorld msg="Sam Arbid" /> -->
        <cv-header :data="data" />
        <!-- {{ data }} -->
    </section>
</template>

<script>
import { HelloWorld, CvHeader } from './components'
import cvData from './data/cvData.json'
import { reactive } from 'vue'
export default {
    name: 'App',
    components: {
        HelloWorld,
        CvHeader,
    },
    setup() {
        const data = reactive(cvData)

        return {
            data,
        }
    },
}
</script>
