<template>
  <main>
    <section class="banner">
      <div class="banner-inner container">
        <div class="banner-desc">
          <h1 class="banner-title">
            Покупайте фриланс-услуги в
            <span class="banner-title-color">два клика</span>
          </h1>
          <p class="banner-text subtitle">
            Ворк — единица работы продавца, которую можно купить как товар в
            магазине
          </p>
          <input-form buttonName="Найти" placeholder="Что нужно сделать?" />
          <div class="category">
            <p class="category-text">Выберите рубрику, чтобы начать</p>
            <div class="category-block">
              <div class="category-subblock">
                <ui-button
                  class="category-link typography-text"
                  name="Дизайн"
                  :outline="lightgray"
                  :color="black"
                />
                <ui-button
                  class="category-link typography-text"
                  name="Дизайн сайтов"
                  :outline="lightgray"
                  :color="black"
                />
                <ui-button
                  class="category-link typography-text"
                  name="Дизайн логотипа"
                  :outline="lightgray"
                  :color="black"
                />
              </div>
              <div class="category-subblock">
                <ui-button
                  class="category-link typography-text"
                  name="Дизайн визиток"
                  :outline="lightgray"
                  :color="black"
                />
                <ui-button
                  class="category-link typography-text"
                  name="Арт и иллюстрации"
                  :outline="lightgray"
                  :color="black"
                />
                <ui-button
                  class="category-link typography-text"
                  name="Флаера и брошюры"
                  :outline="lightgray"
                  :color="black"
                />
              </div>
              <div class="category-subblock">
                <ui-button
                  class="category-link typography-text"
                  name="Баннеры и стенды"
                  :outline="lightgray"
                  :color="black"
                />
                <ui-button
                  class="category-link typography-text"
                  name="Дизайн презентации"
                  :outline="lightgray"
                  :color="black"
                />
                <ui-button
                  class="category-link typography-text"
                  name="Все подкатегории"
                  :outline="lightgray"
                  :color="black"
                />
              </div>
            </div>
          </div>
        </div>
        <img src="~/assets/img/banner.png" alt="banner" />
      </div>
    </section>
  </main>
</template>

<script>
import colors from "~/assets/styles/parts/_variables.scss";

export default {
  name: "IndexPage",
  data() {
    return {
      lightgray: colors.lightgray,
      black: colors.black,
    };
  },
};
</script>

<style lang="scss" scoped>
.banner {
  padding-top: 38px;
  padding-bottom: 122px;
  background-color: $lightviolet;
}

.banner-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}

.banner-desc {
  max-width: 570px;
}

.banner-title {
  font-size: 36px;
  font-weight: bold;
  line-height: 44px;
  margin-bottom: 30px;
}

.banner-title-color {
  color: $green;
}

.banner-text {
  margin-bottom: 50px;
}

.category {
  margin-top: 50px;
}

.category-text {
  font-size: 16px;
  font-weight: 500;
  line-height: 20px;
  margin-bottom: 30px;
}

.category-block {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.category-subblock {
  display: flex;
  gap: 20px;
}

.category-link {
  white-space: nowrap;

  &:hover {
    border: 1px solid $green !important;
    color: $green !important;
  }

  svg {
    display: none !important;
  }
}
</style>
