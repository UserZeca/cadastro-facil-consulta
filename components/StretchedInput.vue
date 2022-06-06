<template>
  <div>
    <div v-if="checked == false">
      <div class="form-check" >
          <input
              class="form-check-input" type="checkbox"
              value=""
              data-bs-toggle="collapse" data-bs-target="#collapseT"
              aria-expanded="true" aria-controls="collapseT"
          >
          <label class="form-check-label weight-700" for="flexCheckDefault">
              {{labelContent}}
          </label>
      </div>

      <div class="collapse" id="collapseT">
            <div class="form-check spacing-input-radio" v-for="item in radioOptions" :key="item.option" :value="item.option">
              <label class="form-check-label">
                  <input class="form-check-input" type="radio" :name="name">
                  {{item.option}}
              </label>
          </div>
      </div>
    </div>

    <div v-if="checked == true">
      <div class="form-check" >
          <input
              class="form-check-input" type="checkbox"
              value=""
              data-bs-toggle="collapse" data-bs-target="#collapseT"
              aria-expanded="true" aria-controls="collapseT"
              checked
          >
          <label class="form-check-label weight-700" for="flexCheckDefault">
              {{labelContent}}
          </label>
      </div>

      <div class="collapse show" id="collapseT">

            <div class="form-check show spacing-input-radio" v-for="item in radioOptions" :key="item.option" :value="item.option">
              <label class="form-check-label label-input-radio">
                  <input class="form-check-input" type="radio" :name="name">
                  {{item.option}}
              </label>
          </div>
      </div>
    </div>

  </div>
</template>

<script>

   export default {

        name: 'StretchedInput',
        props: {
            radioOptions: Array,
            name: String,
            checked: {
              type: Boolean,
              default: false
            },
            labelContent: {
              type: String,
              default: ''
            }
        }

   }

</script>


<style scoped>

.spacing-input-radio{

  margin-left: 60px;
}



</style>
