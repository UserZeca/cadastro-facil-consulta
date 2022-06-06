<template>
  <main>
    <div class="container-body card">
      <div class="row g-0">
          <h1 class="card-title ">Sobre o Atendimento</h1>

          <div class="col-md-6">
            <div class="card-body">
              <!--<p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer. </p>
              <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
              -->
              <form>

                  <div class="mb-4 row">
                    <div class="col">
                        <SelectOption :items="items" labelContent="Especialidade principal*" />
                      </div>
                  </div>
                  <div>
                    <div class="mb-2">
                      <label>Informe o preço da consulta*</label>
                    </div>
                    <div class="input-group mb-4 ">
                        <span class="input-group-text">$</span>
                        <input type="text" class="form-control" aria-label="Amount (to the nearest dollar)">
                    </div>
                  </div>

                  <div>
                    <div class="mb-3">
                      <label>Formas de pagamento da consulta*</label>
                    </div>
                    <div class="card-check mb-3">
                      <div class="form-check">
                          <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault">
                          <label class="form-check-label weight-700" for="flexCheckDefault">
                              Pix
                          </label>
                      </div>
                    </div>
                  </div>
                  <div class="card-check mb-3">
                    <div class="form-check ">
                        <input class="form-check-input" type="checkbox" value="" id="flexCheckChecked">
                        <label class="form-check-label weight-700" for="flexCheckChecked">
                            Em dinheiro
                        </label>
                    </div>
                  </div>


                  <div class="mb-4 card-check">
                    <StretchedInput :radioOptions="items" labelContent="Cartão de Crédito" name="opcoesdepagamento" :checked="teste"/>
                  </div>

                  <div class="mb-3 row">

                      <div class="col-10">
                          <ProgressBar status="100" min="0" max="100"/>
                      </div>

                      <div class="col-2">
                          <h5>2 de 2</h5>
                      </div>

                  </div>

                  <div  class="mb-3 row">
                      <ProgressButton content="Próximo"/>
                  </div>

              </form>
            </div>

          </div>
          <div class="col-md-6 justify-content-center-column">
            <img src="https://res.cloudinary.com/dyie6o63u/image/upload/v1653663281/desktop-pagina-2_bikyg9.png" class="img-fluid rounded-start " alt="...">
          </div>


      </div>
    </div>
  </main>
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
                    {option: '1x sem juros'},
                    {option: '2x sem juros'},
                    {option: '3x sem juros'}

                ],

                teste: false

            }

        }

    }


</script>


<style>


</style>
