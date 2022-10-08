<template>
  <label>
    <input
      type="text"
      :placeholder="placeholder"
      :class="`input ${noBorders ? 'no-borders' : ''}`"
    />
  </label>
</template>

<script>
export default {
  props: {
    placeholder: String,
  },
};
</script>

<style lang="scss" scoped>
.input {
}
</style>