<template>
  <v-flex xs1>
    <v-combobox
      :items="sizeList"
      item-text="value"
      item-value="value"
      background-color="white"
      v-model="selectedValue"
      dense
      outlined
      @change="changeValue()"
    />
    <div>{{ selectedValue }}</div>
  </v-flex>
  <!-- @change="changeValue()" -->
</template>

<script>
export default {
  name: "comboBox",
  props: ["selectedSize", "sizeList"],

  data() {
    return {
      selectedValue: "",
      savedValue: "",
      list: {},
    };
  },
  mounted() {
    this.selectedValue = this.selectedSize;
  },
  methods: {
    changeValue() {
      this.savedValue = this.selectedValue;
      this.$emit("");
    },
  },
};
</script>
<style scoped>
.v-input__control .v-text-field__details {
  display: none;
}
</style>
