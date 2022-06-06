<template>

  <div class="container-input">
    <label class="form-label">{{labelContent}}</label>

    <input v-if="mask != ''"
      :type="type" :value="value"  v-mask="mask" :minlength="minLength" :maxlength="maxLength"
      class="form-control"  aria-describedby="emailHelp"
      :placeholder="placeHolder ">

    <input v-else
      :type="type" :value="value"  :minlength="minLength" :maxlength="maxLength"
      class="form-control"  aria-describedby="emailHelp" valid
      :placeholder="placeHolder">

    <div class="form-text erro-mensage"> </div>

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


        },




    }


</script>


<style>

input {
  border: 1px solid var(--primary) !important;
}

input:invalid {
  border: 1px solid var(--danger);
}

.erro-mensage{

    color: var(--danger);

}

.container-input{
  min-height: 95px;
}


</style>
