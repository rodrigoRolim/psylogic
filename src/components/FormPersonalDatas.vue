<template>
 <v-form
    ref="form"
    v-model="valid"
    lazy-validation
  >
    <v-row>
      <v-col :sm="12">
        <v-text-field
          class="ml-4 mr-4"
          v-model="name"
          :rules="nameRules"
          label="Nome completo"
          required
          outlined
        ></v-text-field>
      </v-col>
    </v-row>
    
    <v-row>
      <v-col :sm="12" :md="4" :lg="4">
        <v-text-field
          class="ml-4 mr-4"
          v-model="birthday"
          :rules="birthdayRules"
          label="Data de nascimento"
          required
          outlined
        ></v-text-field>
      </v-col>
      <v-col :sm="12" :md="4" :lg="4">
        <v-text-field
          class="ml-4 mr-4"
          label="Idade"
          outlined
        ></v-text-field>
      </v-col>
      <v-col :sm="12" :md="4" :lg="4">
        <v-select
          class="ml-4 mr-4"
          v-model="select"
          :items="items"
          :rules="[v => !!v || 'Item is required']"
          label="Sexo"
          required
          outlined
       ></v-select>
      </v-col>
    </v-row>
    <v-row>
      <v-col :sm="12" :lg="6">
        <v-text-field
          class="ml-4 mr-4"
          label="RG"
          outlined
        ></v-text-field>
      </v-col>
      <v-col :sm="12" :lg="6">
        <v-text-field
          class="ml-4 mr-4"
          label="CPF"
          outlined
        ></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-btn
          color="primary"
          @click="click"
        >
          Continue
        </v-btn>
      </v-col>
    </v-row>
  </v-form>  
</template>

<script>
export default {
  data: () => ({
    valid: true,
    name: '',
    nameRules: [
      v => !!v || 'Name is required',
      //v => (v && v.length <= 10) || 'Name must be less than 10 characters',
    ],
    birthday: '',
    birthdayRules: [
      v => !!v || 'campo obrigatório',
      v => /[0-9]{2}\/[0-9]{2}\/[0-9]{4}/.test(v) || 'data de nascimento inválida',
    ],
    select: null,
    items: [
      'masculino',
      'feminino'
    ],
    checkbox: false,
  }),
  methods: {
    validate () {
      this.$refs.form.validate()
    },
    reset () {
      this.$refs.form.reset()
    },
    resetValidation () {
      this.$refs.form.resetValidation()
    },
    click () {
      this.$emit("step", 2)
    }
  },
}
</script>
