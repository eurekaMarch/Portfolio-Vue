<template>
  <section class="home container" id="home">
    <div class="home__intro">
      <img :src="Me" alt="" class="home__img" />
      <h1 class="home__name">Trairat Kaewsaad</h1>
      <span class="home__education">I'm a Full-Stack developer</span>

      <div class="home__socials">
        <a href="https://www.instagram.com/" class="home__link" target="blank"
          ><i class="fa-brands fa-instagram"></i
        ></a>
        <a href="https://www.twitter.com/" class="home__link" target="blank"
          ><i class="fa-brands fa-twitter"></i
        ></a>
        <a href="https://www.behance.com/" class="home__link" target="blank"
          ><i class="fa-brands fa-behance"></i
        ></a>
        <a href="https://www.dribble.com/" class="home__link" target="blank"
          ><i class="fa-brands fa-dribbble"></i
        ></a>
        <a href="https://www.pinterest.com/" class="home__link" target="blank"
          ><i class="fa-brands fa-pinterest"></i
        ></a>
      </div>

      <a href="#contact" class="btn">Hire Me</a>

      <div class="home__scroll-down">
        <a href="#about" class="home__mouse-wrapper">
          <span class="home__scroll-name">Scroll Down</span>
          <span class="home__mouse">
            <span class="home__wheel"></span>
          </span>
        </a>
      </div>
    </div>
    <Shapes />
  </section>
</template>

<script setup>
import Me from "../../assets/reshot-icon-astronaut-54M9J26W7N.svg";
import Shapes from "./Shapes.vue";
</script>

<style scoped>
.home {
  position: relative;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.home__intro {
  max-width: 540px;
  text-align: center;
}

.home__img {
  margin-bottom: 1.5rem;
  width: 150px;
  height: 150px;
}

.home__name {
  font-size: var(--h1-font-size);
  font-weight: var(--font-bold);
  margin-bottom: 0.5rem;
}

.home__socials {
  display: flex;
  column-gap: 1.75rem;
  margin: 1.5rem 0;
  justify-content: center;
}

.home__link {
  color: var(--title-color);
  font-size: 1.3rem;
  transition: 0.3s;
}

.home__link:hover {
  color: hsl(43, 100%, 68%);
}

.home__scroll-down {
  bottom: 2.5rem;
  left: 0;
  width: 100%;
}

.home__scroll-name {
  font-size: var(--small-font-size);
}

.home__mouse {
  border: 2px solid #454360;
  display: block;
  height: 1.6rem;
  width: 1.25rem;
  margin: auto;
  margin-top: 0.75rem;
  border-radius: 1rem;
  position: relative;
}

.home__wheel {
  background-color: var(--title-color);
  border-radius: 50%;
  width: 0.25rem;
  height: 0.25rem;
  position: absolute;
  top: 0.5rem;
  left: 50%;
  transform: translateX(-50%);
  animation: ani-mouse 1.5s linear infinite;
}

@keyframes ani-mouse {
  0% {
    top: 29%;
  }

  15% {
    top: 50%;
  }

  50% {
    top: 50%;
  }

  100% {
    top: 29%;
  }
}
</style>
