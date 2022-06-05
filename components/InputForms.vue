<template>

  <div>
    <label for="exampleInputEmail1" class="form-label">{{labelContent}}</label>

    <input v-if="mask != ''"
      :type="type" :value="value" v-mask="mask" :minlength="minLength" :maxlength="maxLength"
      class="form-control"  aria-describedby="emailHelp"
      :placeholder="placeHolder ">

    <input v-else
      :type="type" :value="value" :minlength="minLength" :maxlength="maxLength"
      class="form-control"  aria-describedby="emailHelp"
      :placeholder="placeHolder">

     <div id="emailHelp" class="form-text"> We'll never share your email with anyone else.</div>

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

            },

            mask: {
              type: String,
              default: ''

            },

            minLength: {
              type: String,
              default: ''

            },

            maxLength: {
              type: String,
              default: ''

            }


        }


    }


</script>


<style>

input {
  border: 2px solid currentcolor;
}
input:invalid {
  border: 2px dashed red;
}
input:invalid:focus {
  background-image: linear-gradient(pink, lightgreen);
}

</style>
