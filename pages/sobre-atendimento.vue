<template>
  <div class="container-body">
    <div class="row g-0">
        <h1 class="card-title ">Sobre o Atendimento</h1>

        <div class="col-md-6">
          <div class="card-body">
            <!--<p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer. </p>
            <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
            -->
            <form>

                <div class="mb-3 row">
                    <div class="col">
                        <SelectOption :items="items" placeHolder="Especialidade principal*"/>
                    </div>
                </div>

                <div class="input-group mb-3">
                    <span class="input-group-text">$</span>
                    <input type="text" class="form-control" aria-label="Amount (to the nearest dollar)">
                    <span class="input-group-text">.00</span>
                </div>


                <div class="form-check">
                    <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault">
                    <label class="form-check-label" for="flexCheckDefault">
                        Default checkbox
                    </label>
                </div>

                <div class="form-check">
                    <input class="form-check-input" type="checkbox" value="" id="flexCheckChecked">
                    <label class="form-check-label" for="flexCheckChecked">
                        Checked checkbox
                    </label>
                </div>

                <StretchedInput :radioOptions="items" name="opcoesdepagamento" :checked="teste"/>


                <div class="mb-3 row">

                    <div class="col-10">
                        <ProgressBar status="100" min="0" max="100"/>
                    </div>

                    <div class="col-2">
                        <h5>1 de 2</h5>
                    </div>

                </div>

                <div  class="mb-3 row">
                    <ProgressButton content="Próximo"/>
                </div>

            </form>
          </div>

        </div>

        <div class="col-md-6 ">
          <img src="https://res.cloudinary.com/dyie6o63u/image/upload/v1653663257/desktop-pagina-1_1_dvtzjh.png" class="img-fluid rounded-start " alt="...">
        </div>

    </div>
  </div>
</template>

<script>

    import SelectOption from '@/components/SelectOption.vue'
    import ProgressBar from '@/components/ProgressBar.vue'
    import StretchedInput from '@/components/StretchedInput.vue'
    import ProgressButton from '@/components/ProgressButton.vue'

    export default {

        name: 'SobreAtendimento',
        components: {
            SelectOption,
            ProgressBar,
            StretchedInput,
            ProgressButton
        },

        data() {

            return {

                items: [
                    {option: 'Chiclete'},
                    {option: 'Pipoca'},
                    {option: 'Feijão Tropeiro'}

                ],

                teste: false

            }

        }

    }


</script>


<style>


</style>
