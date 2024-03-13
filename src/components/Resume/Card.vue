<template>
  <div class="card__timeline">
    <i :class="icon"></i>
    <span class="card__date">{{ year }}</span>
    <h3 class="card__title">{{ title }}</h3>
    <p class="card__text">{{ desc }}</p>
  </div>
</template>

<script setup>
const props = defineProps(["icon", "year", "title", "desc"]);
</script>
