<template>
  <div class="container-body">
    <div class="row g-0" >
        <h1 class="card-title ">Sobre o Profissional {{professional.name}}</h1>
        <div class="col-md-6">
          <div class="card-body">

            <h2>Dados do Profissional</h2>

            <form>
              <div class="mb-3">
                <div class="container-input">
                  <label class="form-label">Nome completo*</label>
                  <input
                    type="type" v-model="name"  minlength="3" maxlength="48"
                    class="form-control"  aria-describedby="emailHelp"
                    placeholder="Digite o nome completo" />
                  <div class="form-text erro-mensage"></div>
                </div>
              </div>

              <div class="mb-3">
                <div class="container-input">
                  <label class="form-label">CPF*</label>
                  <input
                    type="text" v-model="cpf"  minlength="14"
                    class="form-control"  aria-describedby="emailHelp"
                    placeholder="Digite um CPF"
                    v-mask="'###.###.###-##'"
                    >
                  <div class="form-text erro-mensage"> </div>
                </div>
              </div>

              <div class="mb-3">
                <div class="container-input">
                  <label class="form-label">Número de celular*</label>
                  <input
                    type="text" v-model="phone"
                    class="form-control"  aria-describedby="emailHelp"
                    placeholder="(00) 0 0000-0000"
                    v-mask="'(##) #####-####'"
                    />
                  <div class="form-text erro-mensage"> </div>
                </div>

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
                  <ProgressBar status="100" min="0" max="100"/>
                </div>

                <div class="col-2">
                  <h5>1 de 2</h5>
                </div>

              </div>
              <div  class="mb-3 row d-grid gap-2 mx-auto">
                <button @click.prevent="submitForm" class="btn btn-primary">Próximo</button>
                <!--<ProgressButton content="Próximo"/>-->
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

  import useVuelidate from '@vuelidate/core';
  import {required } from 'vuelidate/lib/validators';



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


        v$: useVuelidate(),
        name: '',
        cpf: '',
        phone: '',

      };
    },

    validations: {

        name: { required },
        cpf: {required},
        phone: { required }



    },


    methods: {

      submitForm(){

        console.log(this.v$.value);
        this.v$.value.$validate()

        if(!this.v$.$error){
          alert('Formulário completado com sucesso');
        }else{
          alert('Formulário incompleto');
        }


      }


    }

  }






</script>


<style>

input {
  border: 2px solid var(--primary) !important;
}

input:invalid:not(:focus) {
  border: 2px solid var(--danger) !important;
}

.erro-mensage{
    color: var(--danger);
}

.container-input{
  min-height: 95px;
}




</style>
