<template>
  <button
    v-if="!link"
    :class="`button ${size} ${type} ${outline ? 'outline' : false}`"
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
    outline: {
      type: Boolean,
      default: false,
    },
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
  align-items: center;
  justify-content: center;
  gap: 4px;
  text-align: center;
  width: fit-content;
}

.default {
  color: $white;
  border: none;
  background-color: $green;

  &:hover,
  &:active,
  &:focus {
    background-color: darken($green, 20%);
  }
}

.outline.default {
  border: 1px solid $green;
  color: $green;
  background-color: transparent;

  &:hover {
    background-color: $green;
    color: $white;
  }
}

.outline.secondary {
  border: 1px solid $lightgray;
  color: $black;
  background-color: transparent;

  &:hover {
    color: $green;
    border: 1px solid $green;
    background-color: transparent;
  }
}

.secondary {
  color: $green;
  border: none;
  background-color: $lightgray;

  &:hover,
  &:active,
  &:focus {
    background-color: darken($white, 10%);
  }
}

.accent {
  color: $white;
  border: none;
  background-color: $orange;

  &:hover,
  &:active,
  &:focus {
    background-color: darken($orange, 20%);
  }
}

.no-color {
  border: none;
  background-color: transparent;
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