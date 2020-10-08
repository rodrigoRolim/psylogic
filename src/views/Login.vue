<template>
<v-conteiner class="grey lighten-5">
  <v-row justify="center" align="center">
    <v-col cols="10">
      <v-stepper class="mt-2" v-model="st">
        <v-stepper-header>
          <v-stepper-step
            editable
            step="1"
          >
            dados pessoais
          </v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step
            editable
            step="2"
          >
            endereço
          </v-stepper-step>

          <v-divider></v-divider>

          <v-stepper-step
            step="3"
            editable
          >
            contatos
          </v-stepper-step>
        </v-stepper-header>
        <v-stepper-items>
          <v-stepper-content step="1">
            <form-personal-datas @step="st = $event"/>
          </v-stepper-content>
          <v-stepper-content step="2">
            <form-address @step="st = $event"/>
          </v-stepper-content>
          <v-stepper-content step="3">
            <form-contacts @step="st = $event"/>
          </v-stepper-content>
        </v-stepper-items>
      </v-stepper>
    </v-col>
  </v-row>
</v-conteiner>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import FormPersonalDatas from '@/components/FormPersonalDatas.vue'
import FormAddress from '@/components/FormAddress.vue'
import FormContacts from '@/components/FormContacts.vue'
export default {
  name: 'Home',
  components: {
    FormPersonalDatas,
    FormAddress,
    FormContacts
  },
  data: () => ({
    st: 1
  })
}
</script>
<style scoped>

</style>