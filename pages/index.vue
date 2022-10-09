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
              <ui-button
                v-for="(item, index) in categories"
                :key="index"
                :to="item.link"
                class="category-link typography-text"
                :name="item.name"
                type="secondary"
                :outline="true"
              />
            </div>
          </div>
        </div>
        <img src="~/assets/img/banner.png" alt="banner" />
      </div>
    </section>
    <actual-works />
    <top-freelance />
    <section class="tasks container">
      <h2 class="tasks-title typography-h2">Как решать задачи на WorkTap?</h2>
      <p class="tasks-text typography-text-large">
        Идеально подходит для бизнеса и частных лиц
      </p>
      <div class="tasks-block">
        <div class="tasks-card" v-for="(item, index) in tasks" :key="index">
          <img
            class="tasks-card-image"
            :src="require(`~/assets/img/${item.img}`)"
            alt="step"
          />
          <h3 class="tasks-card-title typography-h3">{{ item.title }}</h3>
          <p class="tasks-card-text typography-text-large">
            {{ item.text }}
          </p>
        </div>
      </div>
    </section>
    <section class="help">
      <div class="help-inner container">
        <div class="help-desc">
          <h2 class="help-title typography-h2">
            Как WorkTap помогает бизнесу?
          </h2>
          <ul class="help-list">
            <li class="help-item">
              <img src="~/assets/img/wallet.svg" alt="wallet" />
              <p class="help-text typography-text">
                Оплачивайте с р/с или карты компании
              </p>
            </li>
            <li class="help-item">
              <img src="~/assets/img/money.svg" alt="money" />
              <p class="help-text typography-text">
                Экономьте до 87% бюджета на фрилансе
              </p>
            </li>
            <li class="help-item">
              <img src="~/assets/img/time.svg" alt="time" />
              <p class="help-text typography-text">
                Экономьте до 75% времени на решении фриланс задач
              </p>
            </li>
          </ul>
          <p class="help-subtitle typography-subtitle">
            WorkTap — быстро, просто и безопасно!
          </p>
          <ui-button
            class="help-button typography-button-large"
            name="Начать!"
          />
        </div>
        <img src="~/assets/img/help.png" alt="help" />
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
      categories: [
        { link: "/", name: "Дизайн" },
        { link: "/", name: "Дизайн сайтов" },
        { link: "/", name: "Дизайн логотипа" },
        { link: "/", name: "Дизайн визиток" },
        { link: "/", name: "Арт и иллюстрации" },
        { link: "/", name: "Флаера и брошюры" },
        { link: "/", name: "Баннеры и стенды" },
        { link: "/", name: "Дизайн презентации" },
        { link: "/", name: "Все подкатегории" },
      ],
      tasks: [
        {
          img: "service.svg",
          title: "Выберите услугу",
          text: "В супермаркете WorkTap представлен широкий выбор услуг от квалифицированных специалистов.",
        },
        {
          img: "payment.svg",
          title: "Оплатите",
          text: "Деньги будут перечислены продавцу после того, как он выполнит работу, и вы её одобрите. ",
        },
        {
          img: "result.svg",
          title: "Получите результат",
          text: "Наш супермаркет гарантирует вам возврат средств в полном объёме в случае невыполнения заказа.",
        },
      ],
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
  max-width: 600px;
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
  flex-wrap: wrap;
  gap: 20px;
}

.category-link {
  white-space: nowrap;
  padding: 10px 20px;

  svg {
    display: none;
  }
}

//tasks
.tasks {
  padding-top: 50px;
  padding-bottom: 100px;
}

.tasks-title {
  margin-bottom: 20px;
}

.tasks-text {
  margin-bottom: 51px;
}

.tasks-block {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}

.tasks-card-image {
  margin-bottom: 19px;
}

.tasks-card-title {
  margin-bottom: 20px;
}

//help
.help {
  width: 100%;
  background: linear-gradient(
    180deg,
    #e2a401 -1.38%,
    #e6a901 17.18%,
    #e3a401 28.99%,
    #e5a800 43.17%,
    #eeb301 77.27%,
    #efb400 100%
  );
  overflow: hidden;
}

.help-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.help-button {
  background-color: #5e4edb;
  border-radius: 50px;
  padding: 20px 60px;
}

.help-desc {
  max-width: 533px;
  width: 100%;
  flex-shrink: 0;
}

.help-title {
  color: $white;
}

.help-list {
  margin-top: 45px;
  margin-bottom: 50px;
  list-style-type: none;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.help-item {
  background-color: $white;
  width: 100%;
  box-shadow: 0px 16px 16px rgba(0, 0, 0, 0.04);
  border-radius: 20px;
  display: flex;
  align-items: center;
  gap: 30px;
  padding: 20px;
}

.help-subtitle {
  color: $white;
  margin-bottom: 40px;
}
</style>
