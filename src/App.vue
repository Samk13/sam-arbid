<template>
    <div class="container m-auto text-gray-900 font-roboto">
        <cv-header :data="data" class="w-full" />
        <div class="flex">
            <cv-body-left :data="data" class="w-2/3" />
            <cv-body-right :data="data" class="w-1/3" />
        </div>
    </div>
</template>

<script>
import { HelloWorld, CvHeader, CvBodyLeft, CvBodyRight } from './components'
import cvData from './data/cvData.json'
import { reactive } from 'vue'
export default {
    name: 'App',
    components: {
        HelloWorld,
        CvHeader,
        CvBodyLeft,
        CvBodyRight,
    },
    setup() {
        const data = reactive(cvData)

        return {
            data,
        }
    },
}
</script>
