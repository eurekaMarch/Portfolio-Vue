<template>
  <section class="testimonials container section">
    <h2 class="section__title">Clients & Reviews</h2>
    <Swiper
      class="testimonials__container grid"
      :modules="modules"
      :space-between="30"
      :slides-per-view="1"
      :loop="true"
      :grabCursor="true"
      :pagination="{ clickable: true }"
    >
      <SwiperSlide
        class="testimonials__item"
        v-for="(item, index) in data"
        :key="index"
      >
        <div class="testimonials__thumb">
          <img :src="item.image" />
        </div>
        <h3 class="testimonials__title">{{ item.title }}</h3>
        <span class="testimonials__subtitle">{{ item.subtitle }}</span>
        <div class="testimonials__comment">{{ item.comment }}</div>
      </SwiperSlide>
    </Swiper>
  </section>
</template>

<script setup>
import Image1 from "../assets/avatar-1.svg";
import Image3 from "../assets/avatar-3.svg";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Pagination } from "swiper/modules";
import "swiper/css";
import "swiper/css/pagination";

const modules = [Pagination];

const data = [
  {
    image: Image1,
    title: "John Doe",
    subtitle: "Product designer at Dribble",
    comment:
      "I enjoy working with the theme and learn so much. You guys make the process fun and interesting. Good luck! 👍",
  },
  {
    image: Image3,
    title: "John Doe",
    subtitle: "Product designer at Dribble",
    comment:
      "I enjoy working with the theme and learn so much. You guys make the process fun and interesting. Good luck! 👍",
  },
];
</script>

<style>
.testimonials__container {
  max-width: 700px;
  margin: auto;
}

.testimonials__item {
  text-align: center;
  padding: 0 1.2rem 1.25rem;
}

.testimonials__thumb {
  height: 5.6rem;
  width: 5.6rem;
  margin: auto;
}

.testimonials__title {
  margin-top: 0.75rem;
}

.testimonials__subtitle {
  color: #8b88b1;
  font-size: var(--small-font-size);
}

.testimonials__comment {
  background-color: var(--container-color);
  padding: 1.875rem;
  box-shadow: var(--shadow);
  border-radius: var(--border-radius);
  position: relative;
  margin-top: 1.5rem;
  margin-bottom: 3rem;
}

.testimonials__comment::before {
  content: "";
  width: 0;
  height: 0;
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  border-bottom: 10px solid var(--container-color);
  position: absolute;
  left: 49.5%;
  top: -0.625rem;
  transform: translateX(-7.5px);
}

.swiper-pagination-bullet {
  width: 0.5rem !important;
  height: 0.375rem !important;
  background-color: var(--first-color) !important;
  opacity: 1 !important;
}

.swiper-pagination-bullet-active {
  width: 1.2rem !important;
  height: 0.375rem !important;
  border-radius: 0.5rem !important;
}
</style>
