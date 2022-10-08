<template>
  <button
    v-if="!link"
    :class="`button ${size} ${type}`"
    :style="`background-color:  ${
      outline ? 'transparent' : background || green
    }; ${outline ? 'border: 1px solid' + outline : ''}; color: ${
      color || white
    }`"
  >
    <ui-icon :name="icon" :width="width" :height="height" :fill="fill" />
    {{ name }}
  </button>
  <nuxt-link :to="link" v-else :class="`button ${size} ${type}`">
    {{ name }}
  </nuxt-link>
</template>

<script>
import colors from "~/assets/styles/parts/_variables.scss";

export default {
  props: {
    name: String,
    size: {
      type: String,
      default: "small",
    },
    type: {
      type: String,
      default: "default",
    },
    link: String,
    background: String,
    outline: String,
    color: String,
    width: Number,
    height: Number,
    fill: String,
    icon: String,
  },
  data() {
    return {
      green: colors.green,
      white: colors.white,
    };
  },
};
</script>

<style lang="scss" scoped>
.button {
  cursor: pointer;
  user-select: none;
  border-radius: 50px;
  outline: none;
  transition: 0.2s;
  display: flex;
  place-items: center;
  gap: 4px;
}

.default {
  color: $white;
  font-weight: 600;
  font-size: 14px;
  line-height: 20px;
  border: none;

  &:hover,
  &:active,
  &:focus {
    background-color: darken($green, 20%);
  }
}

.outline {
  border: 1px solid $green;
  color: $green;
  font-size: 14px;
  line-height: 17px;
  font-weight: 500;
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