<template>
    <div class="text-center bg-blue-600 text-white p-4 mb-10">
        <h2 class="text-3xl md:text-5xl font-bold mb-3">{{text}}</h2>
        <div class="text-2xl mt-4 mb-10">
            {{ timestamp }}
        </div>
    </div>
</template>

<script>
import moment from 'moment'

export default {
    name: 'DataTitle',
    props: ['text', 'dataDate'],
    computed: {
        timestamp: function() {
            return moment(this.dataDate).format('MMMM D YYYY')+ " | " + moment(this.dataDate).format('h:mm:ss a')
        }
    },
}
</script>