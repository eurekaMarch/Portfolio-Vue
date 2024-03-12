<script setup>
import Sidebar from "./components/Sidebar.vue";
import Home from "./components/Home/Home.vue";
import About from "./components/About.vue";
import Services from "./components/Services.vue";
import Resume from "./components/Resume/Resume.vue";
import Portfolio from "./components/Portfolio.vue";
import Pricing from "./components/Pricing.vue";
import Testimonials from "./components/Testimonials.vue";
import Blog from "./components/Blog.vue";
import Contact from "./components/Contact.vue";
</script>

<template>
  <Sidebar />
  <main>
    <Home id="home" />
    <About id="about" />
    <Services id="services" />
    <Resume id="resume" />
    <Portfolio id="portfolio" />
    <Pricing id="pricing" />
    <Testimonials id="testimonials" />
    <Blog id="blog" />
    <Contact id="contact" />
  </main>
</template>

<style scoped>
main {
  margin-left: 110px;
}
</style>
