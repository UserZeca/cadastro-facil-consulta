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
          <label class="form-check-label" for="flexCheckDefault">
              Chocolate
          </label>
      </div>

      <div class="collapse" id="collapseT">

            <div class="form-check" v-for="item in radioOptions" :key="item.option" :value="item.option">
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
          <label class="form-check-label" for="flexCheckDefault">
              Chocolate
          </label>
      </div>

      <div class="collapse show" id="collapseT">

            <div class="form-check show" v-for="item in radioOptions" :key="item.option" :value="item.option">
              <label class="form-check-label">
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
            }
        }

   }

</script>


<style>



</style>
