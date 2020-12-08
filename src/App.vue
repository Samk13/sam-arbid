<template>
    <div class="container mx-auto text-gray-900 font-roboto">
        <!-- <toggle-component class="mt-4" /> -->
        <cv-header :data="data" class="w-full" />
        <div class="flex">
            <cv-body-left :data="data.relevantExperience" class="w-2/3" />
            <cv-body-right :data="data" class="w-1/3" />
        </div>
    </div>
</template>

<script>
import {
    HelloWorld,
    CvHeader,
    CvBodyLeft,
    CvBodyRight,
    // ToggleComponent,
} from './components'
import { ref } from 'vue'
export default {
    name: 'App',
    components: {
        HelloWorld,
        CvHeader,
        CvBodyLeft,
        CvBodyRight,
        // ToggleComponent,
    },
    setup() {
        const data = ref({})

        const getData = () => {
            fetch('./data/cvData.json')
                .then((res) => res.json())
                .then((d) => (data.value = d))
        }
        getData()

        return {
            data,
        }
    },
}
</script>
