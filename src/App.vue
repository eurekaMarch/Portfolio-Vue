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
    <Home />
    <About />
    <Services />
    <Resume />
    <Portfolio />
    <Pricing />
    <Testimonials />
    <Blog />
    <Contact />
  </main>
</template>

<style scoped>
main {
  margin-left: 110px;
}
</style>
