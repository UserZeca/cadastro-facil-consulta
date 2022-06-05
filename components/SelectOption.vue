<template>


  <select class="form-select" aria-label="Default select example">
      <option selected>{{placeHolder}}</option>
      <option v-for="item in items" :key="item.option" :value="item.option">
          {{item.option}}
      </option>

  </select>


</template>

<script>
    export default {
        name: 'SelectOption',
        props: {
            items: Array,
            placeHolder: String,

        },
    }
</script>


<style>



</style>
