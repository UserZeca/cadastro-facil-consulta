<template>


  <div class="card container-body" >
    <div class="row g-0" >
        <h1>Sobre o Profissional {{professional.name}}</h1>

        <div class="col-md-6">
          <div class="card-body">
            <!--<p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer. </p>
            <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
            -->

            <form>
              <div class="mb-3">
                <h4>Dados do profissional</h4>
              </div>
              <div class="mb-3">
                <InputForms type="text"
                  for="a"
                  :value="professional.name"
                  labelContent="Nome completo*"
                  placeHolder="Digite o nome completo"
                  minLength="3"
                  maxLength="48"

                  />

              </div>

              <div class="mb-3">
                <InputForms type="text"
                  for="a"
                  labelContent="CPF"
                  placeHolder="Digite um CPF"
                  mask="###.###.###-##"
                  />
              </div>

              <div class="mb-3">
                <InputForms type="text"
                  id="phone"
                  for="a"
                  labelContent="Número de celular*"
                  placeHolder="(00) 0 0000-0000"
                  mask="(##) #####-####"
                  />
                <!--
                  <label>Phone Number</label>
                  <masked-input
                    type="text"
                    name="phone"
                    class="form-control"
                    v-model="phone"
                    :mask="['(', /[0-9]/, /\d/,')', '9', ' ' , /\d/, /\d/, /\d/, /\d/, '-', /\d/, /\d/, /\d/, /\d/]"
                    :guide="true"
                    placeholderChar="_">
                  </masked-input>
                -->
              </div>

              <div class="mb-3 row">
                <div class="col">
                 <SelectOption :items="items" labelContent="Estado*"/>
                </div>

                <div class="col">
                  <SelectOption :items="items" labelContent="Cidade*"/>
                </div>
              </div>

              <div class="mb-3 row">

                <div class="col-10">
                  <ProgressBar status="50" min="0" max="100"/>
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
    import MaskedInput from 'vue-text-mask';

    //import store from '@/store';
    import {mapState} from 'vuex';




  export default {
    name: 'SobreProfissional',
    components: {
        SelectOption,
        InputForms,
        ProgressBar,
        ProgressButton,
        MaskedInput

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
          name: '',
          phone: ''


      };
    },

  }






</script>


<style>


</style>
