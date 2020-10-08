<template>
<v-form
  ref="form"
  lazy-validation
>
  <v-row>
    <v-col>
      <v-text-field
        outlined
        label="Rua"
      ></v-text-field>
    </v-col>
  </v-row>
  <v-row>
    <v-col>
      <v-text-field
        outlined
        label="Número"
      ></v-text-field>
    </v-col>
    <v-col>
      <v-text-field
        outlined
        label="Complemento"
      ></v-text-field>
    </v-col>
  </v-row>
  <v-row>
    <v-col>
      <v-text-field
        outlined
        label="Bairro"
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
  name: 'FormAddress',
  methods: {
    click () {
      this.$emit("step", 3)
    }
  }
}
</script>

<style scoped>

</style>