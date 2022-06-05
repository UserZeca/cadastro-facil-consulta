<template>

    <div class="progress">
        <div class="progress-bar" :style="`width: ${status}%;`" role="progressbar" :aria-valuenow="status" :aria-valuemin="min" :aria-valuemax="max"></div>
    </div>
</template>


<script>

    export default {
        name: 'ProgressBar',
        props: {
            status: {
                type: String,
                default: '0' 
            },

            min: {
                type: String,
                default: '0'

            },
            max: {
                type: String,
                default: '100'
            }

            
        }

    }

</script>


<style>


</style>