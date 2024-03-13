<template>
  <section class="services container section" id="services">
    <h2 class="section__title">Services</h2>

    <div class="services__container grid">
      <div class="services__card" v-for="(item, index) in data" :key="index">
        <img :src="item.image" alt="" class="services__img" />

        <h3 class="services__title">{{ item.title }}</h3>

        <p class="services__description">{{ item.description }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import Image1 from "../assets/service-1.svg";
import Image2 from "../assets/service-2.svg";
import Image3 from "../assets/service-3.svg";

const data = [
  {
    image: Image1,
    title: "UI/UX design",
    description:
      "Lorem ipsum dolor sit amet consectetuer adipiscing elit aenean commodo ligula eget.",
  },
  {
    image: Image2,
    title: "Web Development",
    description:
      "Lorem ipsum dolor sit amet consectetuer adipiscing elit aenean commodo ligula eget.",
  },
  {
    image: Image3,
    title: "Photography",
    description:
      "Lorem ipsum dolor sit amet consectetuer adipiscing elit aenean commodo ligula eget.",
  },
];
</script>

<style scoped>
.services__container {
  grid-template-columns: repeat(3, 1fr);
  column-gap: 1.875rem;
}

.services__card {
  text-align: center;
  padding: 1.875rem;
  border-radius: var(--border-radius);
  background-color: var(--container-color);
  transition: all 0.3s ease-in-out;
}

.services__card:hover {
  transform: translateY(-10px);
}

.services__card:nth-of-type(1) {
  background-color: rgb(108, 108, 299);
  box-shadow: 0px 5px 20px 0px rgb(108, 108, 299 / 50%);
}
.services__card:nth-of-type(2) {
  background-color: rgb(249, 215, 76);
  box-shadow: 0px 5px 20px 0px rgb(249, 215, 76 / 50%);
}
.services__card:nth-of-type(3) {
  background-color: rgb(249, 123, 139);
  box-shadow: 0px 5px 20px 0px rgb(249, 123, 139 / 50%);
}

.services__img {
  margin-bottom: 1.25rem;
}

.services__title {
  font-size: var(--h3-font-size);
  margin-bottom: 1rem;
  color: #fff;
}

.services__description {
  color: #f8f9fa;
}

.services__card:nth-of-type(2) > .services__title {
  color: var(--title-color);
}

.services__card:nth-of-type(2) > .services__description {
  color: var(--text-color);
}
</style>
