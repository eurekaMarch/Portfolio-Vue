<template>
  <section class="portfolio container section" id="portfolio">
    <h2 class="section__title">Resent Works</h2>

    <div class="portfolio__filters">
      <span class="portfolio__item" @click="() => (data = menu)">
        Everything
      </span>
      <span class="portfolio__item" @click="filterItem('Creative')">
        Creative
      </span>
      <span class="portfolio__item" @click="filterItem('Art')"> Art </span>
      <span class="portfolio__item" @click="filterItem('Design')">
        Design
      </span>
      <span class="portfolio__item" @click="filterItem('Branding')">
        Branding
      </span>
    </div>

    <div class="portfolio__container grid">
      <div class="portfolio__card" v-for="(item, index) in data" :key="index">
        <div class="portfolio__thumnail">
          <img :src="item.image" alt="" class="portfolio__img" />
          <div class="portfolio__mask"></div>
        </div>

        <span class="portfolio__category">{{ item.category }}</span>
        <h3 class="portfolio__title">{{ item.title }}</h3>
        <a href="#" class="portfolio__button">
          <i class="icon-link portfolio__button--icon"></i>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import Work1 from "../assets/work-1.svg";
import Work2 from "../assets/work-2.svg";
import Work3 from "../assets/work-3.svg";
import Work4 from "../assets/work-4.svg";
import Work5 from "../assets/work-5.svg";
import Work6 from "../assets/work-6.svg";

const menu = ref([
  {
    image: Work1,
    title: "Project Management Illustration",
    category: "Design",
  },
  {
    image: Work2,
    title: "Guest App Walkthrough Screens",
    category: "Art",
  },
  {
    image: Work3,
    title: "Delivery App Wireframe",
    category: "Branding",
  },
  {
    image: Work4,
    title: "Onboarding Motivation",
    category: "Design",
  },
  {
    image: Work5,
    title: "iMac Mockup Design",
    category: "Creative",
  },
  {
    image: Work6,
    title: "Game Store App Concept",
    category: "Art",
  },
]);

const data = ref(menu.value);

const filterItem = (categoryItem) => {
  const updateItems = menu.value.filter((curElem) => {
    return curElem.category === categoryItem;
  });
  data.value = updateItems;
};
</script>

<style scoped>
.portfolio__filters {
  display: flex;
  align-items: center;
  column-gap: 1.875rem;
  margin-bottom: 2.5rem;
}

.portfolio__item {
  cursor: pointer;
  font-weight: var(--font-bold);
  transition: 0.3s;
}

.portfolio__item:hover {
  color: var(--first-color);
}

.portfolio__container {
  grid-template-columns: repeat(3, 1fr);
  gap: 1.875rem;
}

.portfolio__card {
  position: relative;
  overflow: hidden;
  border-radius: var(--border-radius);
  box-shadow: var(--shadow);
}

.portfolio__mask {
  background-color: #6c6ce5;
  position: absolute;
  height: 100%;
  width: 100%;
  left: 0;
  top: 0;
  transition: 0.3s;
  opacity: 0;
}

.portfolio__card:hover .portfolio__mask {
  opacity: 0.9;
}

.portfolio__category {
  color: #fff;
  background-color: var(--first-color);
  border-top-left-radius: 0.98rem;
  border-top-right-radius: 0.98rem;
  position: absolute;
  top: 0;
  left: 1.5rem;
  font-size: var(--small-font-size);
  display: inline-block;
  padding: 0.19rem 0.625rem;
  transform: translateY(-40px);
  transition: 0.3s;
}

.portfolio__title {
  color: #fff;
  font-size: var(--h3-font-size);
  margin: 0 0 0.98rem;
  padding: 0 1.25rem;
  position: absolute;
  top: 3.75rem;
  transform: translateY(30px);
  transition: 0.3s;
  opacity: 0;
}

.portfolio__button {
  color: #fff;
  position: absolute;
  bottom: 1.5rem;
  left: 1.5rem;
  font-size: var(--h3-font-size);
  display: block;
  background-color: #ffd15c;
  height: 40px;
  width: 40px;
  border-radius: 50px;
  cursor: pointer;
  text-align: center;
  line-height: 42px;
  transition: 0.3s;
  opacity: 0;
}

.portfolio__card:hover .portfolio__button {
  opacity: 1;
}

.portfolio__card:hover .portfolio__title,
.portfolio__card:hover .portfolio__category {
  opacity: 1;
  transform: translateY(0);
}
</style>
