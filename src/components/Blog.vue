<template>
  <section class="blog container section" id="blog">
    <h2 class="section__title">Latest Posts</h2>

    <div class="blog__container grid">
      <div class="blog__card">
        <div class="blog__thumb">
          <a href=""><span class="blog__category">Reviews</span></a>
          <a href=""><img :src="Image1" class="blog__img" /></a>
        </div>

        <div class="blog__detail">
          <h3 class="blog__title">
            5 Best App Development Tool for Your Projects
          </h3>
          <div class="blog__meta">
            <span>09 February, 2022</span>
            <span class="blog__dot">.</span>
            <span>Bolby</span>
          </div>
        </div>
      </div>

      <div class="blog__card">
        <div class="blog__thumb">
          <a href=""><span class="blog__category">Tutorial</span></a>
          <a href=""><img :src="Image2" class="blog__img" /></a>
        </div>

        <div class="blog__detail">
          <h3 class="blog__title">Common Misconceptions About Payment</h3>
          <div class="blog__meta">
            <span>07 February, 2022</span>
            <span class="blog__dot">.</span>
            <span>Bolby</span>
          </div>
        </div>
      </div>

      <div class="blog__card">
        <div class="blog__thumb">
          <a href=""><span class="blog__category">Business</span></a>
          <a href=""><img :src="Image3" class="blog__img" /></a>
        </div>

        <div class="blog__detail">
          <h3 class="blog__title">3 Things to know about startup business</h3>
          <div class="blog__meta">
            <span>05 February, 2022</span>
            <span class="blog__dot">.</span>
            <span>Bolby</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import Image1 from "../assets/blog-1.svg";
import Image2 from "../assets/blog-2.svg";
import Image3 from "../assets/blog-3.svg";
</script>

<style scoped>
.blog__container {
  grid-template-columns: repeat(3, 1fr);
  column-gap: 1.875rem;
}

.blog__card {
  box-shadow: var(--shadow);
  border-radius: var(--border-radius);
  overflow: hidden;
}

.blog__thumb {
  position: relative;
  overflow: hidden;
}

.blog__img {
  transform: scale(1);
  transition: 0.3s;
}

.blog__thumb:hover .blog__img {
  transform: scale(1.1);
}

.blog__category {
  color: #fff;
  background-color: var(--first-color);
  border-top-left-radius: 0.9375rem;
  border-top-right-radius: 0.9375rem;
  position: absolute;
  top: 0;
  left: 1.5rem;
  font-size: var(--small-font-size);
  display: inline-block;
  padding: 0.125rem 0.5rem;
  z-index: 1;
  transition: 0.3s;
}

.blog__detail {
  background-color: var(--container-color);
  padding: 1.25rem;
}

.blog__title {
  font-size: var(--h3-font-size);
  margin-bottom: 0.5rem;
}

.blog__meta {
  display: flex;
  column-gap: 0.6rem;
  font-size: var(--small-font-size);
  color: #8b88b1;
}

.blog__dot {
  font-weight: var(--font-bold);
}
</style>
