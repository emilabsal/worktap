<template>
  <div class="freelance">
    <div class="freelance-inner">
      <div class="freelance-image-wrapper">
        <img
          class="freelance-image"
          src="~/assets/img/freelancer.png"
          alt="freelancer"
        />
      </div>
      <div class="freelance-desc">
        <span class="freelance-name typography-input">Марина Королёва</span>
        <span class="freelance-job typography-h3">Разработчик PHP</span>
        <p class="freelance-text typography-text">Выполнено проектов: 65</p>
        <ui-icon name="rating" v-for="item in 5" />
      </div>
    </div>
    <ui-button class="freelance-link" name="Написать" :outline="true" />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.freelance {
  padding: 20px 25px;
  border: 1px solid $lightgray;
  border-radius: 20px;
}

.freelance-inner {
  display: flex;
  align-items: center;
  gap: 29px;
  margin-bottom: 30px;
}

.freelance-image {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  flex-shrink: 0;
}

.freelance-image-wrapper {
  width: 150px;
  height: 150px;
  position: relative;
  flex-shrink: 0;

  &::after {
    content: "";
    position: absolute;
    bottom: 0;
    right: 30px;
    width: 19px;
    height: 19px;
    border-radius: 50%;
    background-color: $green;
  }
}

.freelance-name {
  margin-bottom: 12px;
  display: block;
}

.freelance-job {
  display: block;
  color: $orange;
  margin-bottom: 10px;
}

.freelance-text {
  margin-bottom: 10px;
}

.freelance-link {
  width: 100%;
}
</style>