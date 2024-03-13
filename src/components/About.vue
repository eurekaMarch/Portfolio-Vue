<template>
  <section class="about container section" id="about">
    <h2 class="section__title">About Me</h2>

    <div class="about__container grid">
      <img :src="Profile" alt="" class="about__image" />

      <div class="about__data grid">
        <div class="about__info">
          <p class="about__description">
            I am Trairat Kaewssad, web developer from Thailand. I have rich
            experience in web site design and building and customization, also I
            am good at WordPress.
          </p>
          <a href="" class="btn"> Download CV </a>
        </div>

        <div class="about__skills grid">
          <div class="about__skills--data">
            <div class="about__skills--titles">
              <h3 class="about__skills--name">Development</h3>
              <span class="about__skills--number">90%</span>
            </div>

            <div class="about__skills--bar">
              <span class="about__skills--percentage development"></span>
            </div>
          </div>

          <div class="about__skills--data">
            <div class="about__skills--titles">
              <h3 class="about__skills--name">UI/UX design</h3>
              <span class="about__skills--number">80%</span>
            </div>

            <div class="about__skills--bar">
              <span class="about__skills--percentage ui__design"></span>
            </div>
          </div>

          <div class="about__skills--data">
            <div class="about__skills--titles">
              <h3 class="about__skills--name">Photography</h3>
              <span class="about__skills--number">60%</span>
            </div>

            <div class="about__skills--bar">
              <span class="about__skills--percentage photography"></span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="about__boxes grid">
      <div class="about__box">
        <i class="about__icon icon-fire"></i>

        <div>
          <h3 class="about__title">198</h3>
          <span class="about__subtitle">Project completed</span>
        </div>
      </div>

      <div class="about__box">
        <i class="about__icon icon-cup"></i>

        <div>
          <h3 class="about__title">5670</h3>
          <span class="about__subtitle">Cup of coffee</span>
        </div>
      </div>

      <div class="about__box">
        <i class="about__icon icon-people"></i>

        <div>
          <h3 class="about__title">427</h3>
          <span class="about__subtitle">Satisfied clients</span>
        </div>
      </div>

      <div class="about__box">
        <i class="about__icon icon-badge"></i>

        <div>
          <h3 class="about__title">35</h3>
          <span class="about__subtitle">Nominees winner</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import Profile from "../assets/reshot-icon-black-hair-Z8GE2SCDPX.svg";
</script>

<style scoped>
.about__image {
  width: 150px;
  height: 150px;
}

.about__container {
  grid-template-columns: 3fr 9fr;
  column-gap: 1.875rem;
}

.about__data {
  padding: 1.875rem;
  background-color: var(--container-color);
  box-shadow: var(--shadow);
  border-radius: var(--border-radius);
  grid-template-columns: repeat(2, 1fr);
  column-gap: 1.875rem;
  align-items: flex-start;
  position: relative;
}

.about__data::before {
  content: "";
  width: 0;
  height: 0;
  border-top: 10px solid transparent;
  border-bottom: 10px solid transparent;
  border-right: 15px solid var(--container-color);
  position: absolute;
  left: -0.03rem;
  top: 20%;
}

.about__description {
  margin-bottom: 1rem;
  text-align: justify;
}

.about__skills {
  row-gap: 1.25rem;
}

.about__skills--titles {
  display: flex;
  justify-content: space-between;
}

.about__skills--name {
  font-size: var(--normal-font-size);
  font-weight: var(--font-bold);
}

.about__skills--number {
  line-height: 1.2;
}

.about__skills--bar,
.about__skills--percentage {
  height: 7px;
  border-radius: 0.25rem;
}

.about__skills--bar {
  background-color: #f1f1f1;
}

.about__skills--percentage {
  display: block;
}

.development {
  width: 90%;
  background-color: rgb(255, 209, 92);
}

.ui__design {
  width: 80%;
  background-color: rgb(255, 76, 96);
}

.photography {
  width: 60%;
  background-color: rgb(108, 108, 299);
}

.about__boxes {
  grid-template-columns: repeat(4, 1fr);
  column-gap: 1.875rem;
  margin-top: 4.25rem;
}

.about__box {
  display: flex;
  column-gap: 1.5rem;
}

.about__icon {
  font-size: var(--h1-font-size);
  color: #dedeea;
}

.about__title {
  font-size: 1.875rem;
}
</style>
