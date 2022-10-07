<template>
  <button
    v-if="!link"
    :class="'button ' + (size || 'small') + ' ' + (type || 'default')"
  >
    {{ name }}
  </button>
  <nuxt-link
    :to="link"
    v-else
    :class="'button ' + (size || 'small') + ' ' + (type || 'default')"
  >
    {{ name }}
  </nuxt-link>
</template>

<script>
export default {
  props: {
    name: String,
    size: String,
    type: String,
    link: String,
  },
};
</script>

<style lang="scss" scoped>
.button {
  cursor: pointer;
  border-radius: 50px;
  outline: none;
  transition: 0.2s;
}

.default {
  background-color: $green;
  border: 1px solid $green;
  color: $white;
  font-weight: 600;
  font-size: 14px;
  line-height: 20px;

  &:hover,
  &:active,
  &:focus {
    background-color: darken($green, 20%);
  }
}

.outline {
  border: 1px solid $green;
  color: $green;
  background-color: transparent;
  font-size: 14px;
  line-height: 17px;
  font-weight: 500;

  &:hover {
    background-color: $green;
    color: $white;
  }
}

.no-color {
  border: none;
  background-color: transparent;
  font-size: 16px;
  line-height: 20px;
  color: $black;
}

.inline {
  padding: 0;
}

.small {
  padding: 10px 30px;
}

.medium {
  padding: 20px 50px;
}

.large {
  padding: 20px 60px;
}
</style>