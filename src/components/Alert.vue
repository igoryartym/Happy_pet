<template>
  <v-alert
    dense
    outlined
    dismissible
    type="error"
    @input="onClose"
    :value="true"
    >{{ text }}</v-alert
  >
</template>

<script>
export default {
  name: "Alert",
  props: ["text"],
  methods: {
    onClose() {
      this.$emit("dismissed");
    },
  },
};
</script>

<style lang="scss" scoped></style>
