<template>
  <div class="container-body">
    <div class="row g-0" style="padding: 20px;">
        <h1 class="card-title ">Sobre o Atendimento</h1>
            <div class="col-md-6">
                <div class="card-body">

                    <div>
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
                    </div>

                  <button v-on:click="a"> TESTE</button>
                </div>
            </div>
    </div>
  </div>


</template>



<script>


    import MaskedInput from 'vue-text-mask';

    export default {

      name: 'RevisaoCadastro',

        components: {
        MaskedInput
      },

      data () {
        return {
          phone: '99 9 9999 9999'
        }
      },

      methods: {

        a(){

          console.log(this.phone.replace(/\D/g,''));

        },


      }




    }

</script>


<style>

.erro{

  border: 2px solid red;

}

</style>
