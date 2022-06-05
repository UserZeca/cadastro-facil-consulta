<template>

    <div class="d-grid gap-2 mx-auto">
        <button :type="type" class="btn btn-primary">{{content}}</button>
    </div>

</template>


<script>

    export default {

        name: 'ProgressButton',
        props: {

            type: {
                type: String,
                default: 'button'

            },
            content: {
                type: String,
                default: ''

            }

        }

    }


</script>
