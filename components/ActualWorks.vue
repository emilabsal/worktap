<template>
  <div class="works container">
    <h2 class="works-title typography-h2">Актуальные ворки</h2>
    <div class="works-block">
      <card-work-preview v-for="item in 5" />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.works {
  padding-top: 120px;
  padding-bottom: 50px;
}

.works-title {
  margin-bottom: 48px;
}

.works-block {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
  gap: 30px;
}
</style>