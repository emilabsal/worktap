<template>
  <div class="top container">
    <h2 class="top-title typography-h2">Топ фрилансеров</h2>
    <div class="top-block">
      <card-top-freelance-preview v-for="item in 5" />
      <nuxt-link to="/" class="top-more typography-h3"
        >Посмотреть всех ТОП фрилансеров</nuxt-link
      >
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.top {
  padding-bottom: 50px;
  padding-top: 50px;
}

.top-title {
  display: inline-block;
  margin-bottom: 40px;
}

.top-block {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
  gap: 30px;
}

.top-more {
  text-decoration: none;
  border-radius: 20px;
  background-color: #f2f0fe;
  display: flex;
  align-items: center;
  justify-content: center;
  color: $green;
  padding: 20px;
}
</style>