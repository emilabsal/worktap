<template>
  <footer class="footer">
    <div class="footer-inner container">
      <div class="footer-grid">
        <div class="footer-col">
          <span class="footer-title typography-button-large"
            >Топ категории</span
          >
          <ul class="footer-list">
            <li class="footer-item" v-for="(item, index) in col1">
              <ui-button
                :key="index"
                :to="item.link"
                class="footer-link typography-text"
                :name="item.name"
                type="no-color"
                size="inline"
              />
            </li>
          </ul>
        </div>
        <div class="footer-col">
          <span class="footer-title typography-button-large">О Проекте</span>
          <ul class="footer-list">
            <li class="footer-item" v-for="(item, index) in col2">
              <ui-button
                :key="index"
                :to="item.link"
                class="footer-link typography-text"
                :name="item.name"
                type="no-color"
                size="inline"
              />
            </li>
          </ul>
        </div>
        <div class="footer-col">
          <span class="footer-title typography-button-large">Поддержка</span>
          <ul class="footer-list">
            <li class="footer-item">
              <ui-button
                v-for="(item, index) in col3"
                :key="index"
                :to="item.link"
                class="footer-link typography-text"
                :name="item.name"
                type="no-color"
                size="inline"
              />
            </li>
          </ul>
        </div>
        <div class="footer-col">
          <span class="footer-title typography-button-large">Follow</span>
          <div class="footer-social">
            <ui-button to="/" icon="facebook" type="no-color" size="inline" />
            <ui-button to="/" icon="twitter" type="no-color" size="inline" />
            <ui-button to="/" icon="instagram" type="no-color" size="inline" />
            <ui-button to="/" icon="linkedin" type="no-color" size="inline" />
          </div>
        </div>
      </div>
      <p class="footer-copyright typography-input">
        Copyright @ 2021 | WorkTap – Worktap.KZ. All Rights Reserved
      </p>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      col1: [
        { link: "/", name: "Тексты и переводы" },
        { link: "/", name: "Разработка" },
        { link: "/", name: "Дизайн" },
        { link: "/", name: "Аудио, видео монтаж" },
        { link: "/", name: "Соцсети и реклама" },
        { link: "/", name: "Бизнес и жизнь" },
        { link: "/", name: "SEO и оптимизация" },
      ],
      col2: [
        { link: "/", name: "О Нас" },
        { link: "/", name: "Как Это Работает" },
        { link: "/", name: "Политика Приватности" },
        { link: "/", name: "Правила Пользования " },
        { link: "/", name: "Пресса о нас" },
      ],
      col3: [
        { link: "/", name: "Контакты" },
        { link: "/", name: "Политика Безопасности" },
        { link: "/", name: "FAQ" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.footer {
  padding-top: 50px;
  padding-bottom: 100px;
  background-color: $lightgray;
}

.footer-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
}

.footer-title {
  display: inline-block;
  margin-bottom: 30px;
}

.footer-list {
  list-style-type: none;
}

.footer-item:not(:last-child) {
  margin-bottom: 10px;
}

.footer-social {
  display: flex;
  align-items: center;
  gap: 30px;
}

.footer-copyright {
  margin-top: 50px;
  text-align: center;
}
</style>