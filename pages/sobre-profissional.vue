<template>
  <div class="container-body">
    <div class="row g-0" >
        <h1 class="card-title ">Sobre o Profissional</h1>

        <div class="col-md-6">
          <div class="card-body">
            <!--<p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer. </p>
            <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
            -->
            <form>
              <div class="mb-3">
                <InputForms type="text"
                  for="a"
                  :value="professional.name"
                  labelContent="Nome completo*"
                  placeHolder="Digite o nome completo"/>
                <div id="emailHelp" class="form-text"> We'll never share your email with anyone else.</div>
              </div>

              <div class="mb-3">
                <InputForms type="text"
                  for="a"
                  labelContent="CPF"
                  placeHolder="Digite um CPF"
                  />
              </div>

              <div class="mb-3">
                <InputForms type="text"
                  for="a"
                  labelContent="Número de celular*"
                  placeHolder="(00) 0 0000-0000"/>
              </div>

              <div class="mb-3 row">
                <div class="col">
                 <SelectOption :items="items" placeHolder="Estado*"/>
                </div>

                <div class="col">
                  <SelectOption :items="items" placeHolder="Cidade*"/>
                </div>
              </div>

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

    import SelectOption from '../components/SelectOption.vue'
    import InputForms from '../components/InputForms.vue';
    import ProgressBar from '../components/ProgressBar.vue';
    import ProgressButton from '../components/ProgressButton.vue';
    //import store from '@/store';
    import {mapState} from 'vuex';




  export default {
    name: 'SobreProfissional',
    components: {
        SelectOption,
        InputForms,
        ProgressBar,
        ProgressButton

    },

    computed: {
      ...mapState({

        professional: state => state.professionalInformation

      })

    },

    data() {
      return {
          items: [
              { option: "Pizza" },
              { option: "Outro" }
          ],



      };
    },

  }






</script>


<style>



</style>
