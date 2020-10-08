<template>
  <v-form
    ref="form"
    lazy-validation
  >
    <v-row>
      <v-col>
        <v-text-field
          outlined
          label="Telefone 1"
        ></v-text-field>
      </v-col>
      <v-col>
        <v-text-field
          outlined
          label="Telefone 2"
        ></v-text-field>
      </v-col>
      <v-col>
        <v-text-field
          outlined
          label="Telefone 3"
        ></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-text-field
          outlined
          label="Email"
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
  name: "FormContacts",
  methods: {
    click () {
      this.$emit("step", 1)
    }
  }
}
</script>

<style scoped>

</style>