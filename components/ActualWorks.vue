<template>
  <div class="works container">
    <h2 class="works-title typography-h2">Актуальные ворки</h2>
    <div class="works-block">
      <card-work-preview v-for="(item, index) in 5" :key="index" />
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

@include media-breakpoint-lg {
  .works-block {
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
  }
}
</style>