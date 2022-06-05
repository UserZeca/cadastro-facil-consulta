<template>

<div>
  <label  class="form-check-label">{{labelContent}}</label>

  <select class="form-select" aria-label="Default select example">
      <option selected>Selecione</option>

      <option v-for="item in items" :key="item.option" :value="item.option">
          {{item.option}}
      </option>

  </select>
</div>

</template>

<script>
    export default {
        name: 'SelectOption',
        props: {
            items: Array,
            labelContent: String,

        },
    }
</script>


<style scoped>

  label{

    margin-bottom: 8px;

  }

</style>
