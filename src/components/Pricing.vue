<template>
  <section class="pricing container section">
    <h2 class="section__title">Pricing Plans</h2>

    <div class="pricing__container grid">
      <div class="pricing__item">
        <img :src="Image1" alt="" class="pricing__img" />
        <h3 class="pricing__plan">Basic</h3>
        <p class="pricing__title">
          A Simple option but powerful to manage your business
        </p>
        <p class="pricing__support">Email support</p>
        <h3 class="pricing__price"><sup>$</sup> 9 <span>Month</span></h3>
        <a href="" class="btn">Get Started</a>
      </div>

      <div class="pricing__item pricing__best">
        <span class="pricing__badge">Recommended</span>
        <img :src="Image2" alt="" class="pricing__img" />
        <h3 class="pricing__plan">Premium</h3>
        <p class="pricing__title">
          Unlimited product including app integration and more features
        </p>
        <p class="pricing__support">Mon-Fri support</p>
        <h3 class="pricing__price"><sup>$</sup> 49 <span>Month</span></h3>
        <a href="" class="btn">Get Started</a>
      </div>

      <div class="pricing__item">
        <img :src="Image3" alt="" class="pricing__img" />
        <h3 class="pricing__plan">Ultimate</h3>
        <p class="pricing__title">
          A wise option for large companies and individuals
        </p>
        <p class="pricing__support">24/7 support</p>
        <h3 class="pricing__price"><sup>$</sup> 99 <span>Month</span></h3>
        <a href="" class="btn">Get Started</a>
      </div>
    </div>
  </section>
</template>

<script setup>
import Image1 from "../assets/price-1.svg";
import Image2 from "../assets/price-2.svg";
import Image3 from "../assets/price-3.svg";
</script>

<style scoped>
.pricing__container {
  grid-template-columns: repeat(3, 1fr);
  align-items: center;
}

.pricing__item {
  padding: 1.875rem 2.5rem;
  background-color: var(--container-color);
  text-align: center;
  border-radius: var(--border-radius);
  box-shadow: var(--shadow);
}

.pricing__plan {
  margin: 1.25rem 0;
  font-size: var(--h2-font-size);
}

.pricing__support,
.pricing__title {
  margin-bottom: 1rem;
}

.pricing__price {
  font-size: var(--h1-font-size);
  font-weight: var(--font-bold);
}

.pricing__price sup {
  font-style: normal;
  font-size: var(--small-font-size);
  margin-right: 0.1rem;
}

.pricing__price span {
  font-size: var(--normal-font-size);
  font-weight: 400;
  margin-left: 0.1rem;
}

.pricing__item .btn {
  margin-top: 1.25rem;
}

.pricing__best {
  padding: 3.4rem 2.5rem;
  position: relative;
  z-index: 1;
}

.pricing__badge {
  position: absolute;
  left: 0;
  top: 2.6rem;
  color: #fff;
  background-color: #6c6ce5;
  transform: rotate(-90deg);
  padding: 0.25rem 0.75rem;
  font-size: var(--small-font-size);
  border-top-left-radius: var(--border-radius);
  border-bottom-left-radius: var(--border-radius);
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}
</style>
