<template>

    <div>
        <label for="exampleInputEmail1" class="form-label">{{labelContent}}</label>
        <input :type="type" :value="value" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" :placeholder="placeHolder">
    </div>

</template>

<script>

    export default {

        name: 'InputForms',
        props: {
            type: {
                type: String,
                default: 'text'
            } ,
            for: {
                type: String,
                required: true
            },

            labelContent: {
                type: String,
                default: ''
            },

            placeHolder: {
                type: String,
                default: ''
            },

            value: {

              type: String,
              default: ''

            }


        }


    }


</script>


<style>

</style>
