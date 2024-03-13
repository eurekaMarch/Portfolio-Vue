Resume
<template>
  <section class="resume container section" id="resume">
    <h2 class="section__title">Experience</h2>

    <div class="resume__container grid">
      <div class="resume__timeline grid">
        <Card
          v-for="(item, index) in Data.filter(
            (data) => data.category === 'education'
          )"
          :key="index"
          :icon="item.icon"
          :year="item.year"
          :title="item.title"
          :desc="item.desc"
        />
      </div>

      <div class="resume__timeline grid">
        <Card
          v-for="(item, index) in Data.filter(
            (data) => data.category === 'experience'
          )"
          :key="index"
          :icon="item.icon"
          :year="item.year"
          :title="item.title"
          :desc="item.desc"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
import Card from "./Card.vue";

const Data = [
  {
    category: "education",
    icon: "icon-graduation",
    year: "2019 - present",
    title: "Academic Degree",
    desc: "Lorem ipsum dolor sit amet quo ei simul congue exerciad nec admodum perfecto.",
  },
  {
    category: "education",
    icon: "icon-graduation",
    year: "2013 - 2017",
    title: "Bachelor's Degree",
    desc: "Lorem ipsum dolor sit amet quo ei simul congue exerciad nec admodum perfecto.",
  },
  {
    category: "education",
    icon: "icon-graduation",
    year: "2009 - 2013",
    title: "Honours Degree",
    desc: "Lorem ipsum dolor sit amet quo ei simul congue exerciad nec admodum perfecto.",
  },
  {
    category: "experience",
    icon: "icon-briefcase",
    year: "2019 - present",
    title: "Web Designer",
    desc: "Lorem ipsum dolor sit amet quo ei simul congue exerciad nec admodum perfecto.",
  },
  {
    category: "experience",
    icon: "icon-briefcase",
    year: "2013 - 2017",
    title: "Front-End Developer",
    desc: "Lorem ipsum dolor sit amet quo ei simul congue exerciad nec admodum perfecto.",
  },
  {
    category: "experience",
    icon: "icon-briefcase",
    year: "2009 - 2013",
    title: "Back-End Developer",
    desc: "Lorem ipsum dolor sit amet quo ei simul congue exerciad nec admodum perfecto.",
  },
];
</script>

<style>
.resume__container {
  grid-template-columns: repeat(2, 1fr);
  column-gap: 1.875rem;
}

.resume__timeline {
  background-color: var(--container-color);
  padding: 1.875rem;
  border-radius: var(--border-radius);
  position: relative;
  box-shadow: var(--shadow);
}

.card__timeline {
  position: relative;
  padding-left: 3.125rem;
  padding-bottom: 3.125rem;
}

.card__timeline:last-of-type {
  padding-bottom: 0;
}

.card__timeline::before {
  content: "";
  width: 1px;
  height: 100%;
  background-color: var(--first-color);
  position: absolute;
  left: 0.25rem;
  top: 0;
}

.resume__timeline .icon-graduation,
.resume__timeline .icon-briefcase {
  position: absolute;
  left: -0.4375rem;
  top: 0;
  font-size: var(--h2-font-size);
  color: var(--first-color);
  background-color: var(--container-color);
  padding: 0.4375rem 0;
}
</style>
