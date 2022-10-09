<template>
  <div class="input-form">
    <input
      class="input-form-field typography-input"
      type="text"
      :placeholder="placeholder"
    />
    <ui-button :name="buttonName" type="accent" />
  </div>
</template>

<script>
import colors from "~/assets/styles/parts/_variables.scss";

export default {
  props: {
    buttonName: String,
    placeholder: String,
  },
  data() {
    return {
      orange: colors.orange,
    };
  },
};
</script>

<style lang="scss" scoped>
.input-form {
  background-color: $lightgray;
  display: inline-flex;
  padding: 3px;
  border-radius: 50px;
}

.input-form-field {
  background-color: transparent;
  border: none;
  outline: none;
  color: $black;
  padding: 0 13px;
}

.input-form-field::placeholder {
  color: $darkgray;
}
</style>