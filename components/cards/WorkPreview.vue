<template>
  <nuxt-link to="/" class="work">
    <div class="work-top">
      <img class="work-image" src="~/assets/img/avatar.png" alt="avatar" />
      <h3 class="work-title typography-h3">Сделать дизайн интернет-магазина</h3>
    </div>
    <p class="work-text typography-text-14">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam sed leo
      at hendrerit dictum diam, enim. Dolor in imperdiet ultrices mauris. Est
      vitae vulputate est nec cras. Turpis nunc ornare nulla neque, interdum. At
      pharetra consectetur nec est convallis...
    </p>
    <ui-button
      to="/"
      class="work-link"
      name="Посмотреть"
      type="default"
      :outline="true"
    />
  </nuxt-link>
</template>

<script>
import colors from "~/assets/styles/parts/_variables.scss";

export default {
  data() {
    return {
      green: colors.green,
    };
  },
};
</script>

<style lang="scss" scoped>
.work {
  border: 1px solid $lightgray;
  border-radius: 20px;
  padding: 20px;
  text-decoration: none;
  transition: 0.3s;

  &:hover {
    box-shadow: 0px 16px 16px rgba(34, 34, 34, 0.04);
    transform: translateY(-10px);
  }
}

.work-top {
  display: flex;
  align-items: center;
  gap: 20px;
  margin-bottom: 30px;
}

.work-image {
  width: 44px;
  height: 44px;
  border-radius: 50%;
  object-fit: cover;
  object-position: center;
  flex-shrink: 0;
}

.work-text {
  margin-bottom: 30px;
}
.work-link {
  width: 100%;
}
</style>