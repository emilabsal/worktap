<template>
  <header class="header">
    <div class="header-inner container">
      <button
        :class="`mobile-menu ${open ? 'mobile-menu-active' : ''}`"
        @click="open = !open"
      >
        <span class="mobile-menu-item"></span>
        <span class="mobile-menu-item"></span>
        <span class="mobile-menu-item"></span>
      </button>
      <div class="header-left">
        <nuxt-link to="/" class="header-logo">
          <img class="logo" src="~/assets/img/logo.svg" alt="logo" />
        </nuxt-link>
        <nav class="nav">
          <ul class="nav-list">
            <li class="nav-item" v-for="(item, index) in menu" :key="index">
              <ui-button
                class="nav-link"
                :link="item.link"
                :name="item.name"
                type="no-color"
                size="inline"
              />
            </li>
          </ul>
        </nav>
      </div>
      <div class="header-links">
        <ui-button
          class="header-reg typography-input"
          type="secondary"
          name="Регистрация"
        />
        <ui-button class="typography-input" name="Войти" />
      </div>
      <ui-button
        class="header-enter typography-input"
        name="Вход"
        type="no-color"
        size="inline"
      />
    </div>
  </header>
</template>

<script>
import colors from "~/assets/styles/parts/_variables.scss";

export default {
  data() {
    return {
      green: colors.green,
      lightgray: colors.lightgray,
      open: false,
      menu: [
        { link: "/", name: "Биржа" },
        { link: "/", name: "Ворки" },
        { link: "/", name: "Конкурсы" },
        { link: "/", name: "Создать ворк" },
        { link: "/", name: "Создать заказ" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.header {
  background-color: $lightviolet;
}

.header-inner {
  padding-top: 20px;
  padding-bottom: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header-left {
  display: flex;
  align-items: center;
}

.nav-list {
  display: flex;
  list-style-type: none;
  margin-left: 60px;
}

.nav-link {
  text-decoration: none;
  margin: 0 20px;
}

.header-links {
  display: flex;
  align-items: center;
  gap: 30px;
}

.mobile-menu {
  display: none;
  background-color: transparent;
  border: none;
  flex-direction: column;
  align-items: flex-start;
  gap: 5px;
}

.mobile-menu-item {
  display: inline-block;
  width: 20px;
  height: 2px;
  background-color: $black;
  transition: 0.3s;
}

.mobile-menu-item:nth-child(2) {
  transition: 0.1s;
}

.header-enter {
  display: none;
}

.mobile-menu-active {
  .mobile-menu-item:nth-child(2) {
    visibility: hidden;
  }

  .mobile-menu-item:first-child {
    transform: translateY(7px) rotateZ(45deg);
  }

  .mobile-menu-item:last-child {
    transform: translateY(-7px) rotateZ(-45deg);
  }
}

@include media-breakpoint-lg {
  .header-links {
    display: none;
  }
  .nav {
    display: none;
  }

  .header-enter {
    display: flex;
  }

  .mobile-menu {
    display: flex;
  }
}

@include media-breakpoint-xs {
  .logo {
    width: 150px;
  }
}
</style>