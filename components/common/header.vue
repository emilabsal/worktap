<template>
  <header class="header">
    <div class="header-inner container">
      <div class="header-left">
        <nuxt-link to="/" class="header-logo">
          <img src="~/assets/img/logo.svg" alt="logo" />
        </nuxt-link>
        <nav class="nav">
          <ul class="nav-list">
            <li class="nav-item">
              <ui-button
                class="nav-link"
                link="/"
                name="Биржа"
                type="no-color"
                size="inline"
              />
            </li>
            <li class="nav-item">
              <ui-button
                class="nav-link"
                link="/"
                name="Ворки"
                type="no-color"
                size="inline"
              />
            </li>
            <li class="nav-item">
              <ui-button
                class="nav-link"
                link="/"
                name="Конкурсы"
                type="no-color"
                size="inline"
              />
            </li>
            <li class="nav-item">
              <ui-button
                class="nav-link"
                link="/"
                name="Создать ворк"
                type="no-color"
                size="inline"
              />
            </li>
            <li class="nav-item">
              <ui-button
                class="nav-link"
                link="/"
                name="Создать заказ"
                type="no-color"
                size="inline"
              />
            </li>
          </ul>
        </nav>
      </div>
      <div class="header-links">
        <ui-button class="header-reg" type="secondary" name="Регистрация" />
        <ui-button name="Войти" />
      </div>
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
</style>