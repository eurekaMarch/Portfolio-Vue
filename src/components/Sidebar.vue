<template>
  <aside class="sidebar">
    <a href="#home" class="sidebar__logo">
      <img :src="Logo" />
    </a>

    <nav class="sidebar__nav">
      <div class="sidebar__menu">
        <ul class="sidebar__list">
          <li class="sidebar__item">
            <a href="#home" class="sidebar__link">
              <i class="icon-home"></i>
            </a>
          </li>

          <li class="sidebar__item">
            <a href="#about" class="sidebar__link">
              <i class="icon-user-following"></i>
            </a>
          </li>

          <li class="sidebar__item">
            <a href="#services" class="sidebar__link">
              <i class="icon-briefcase"></i>
            </a>
          </li>

          <li class="sidebar__item">
            <a href="#resume" class="sidebar__link">
              <i class="icon-graduation"></i>
            </a>
          </li>

          <li class="sidebar__item">
            <a href="#portfolio" class="sidebar__link">
              <i class="icon-layers"></i>
            </a>
          </li>

          <li class="sidebar__item">
            <a href="#blog" class="sidebar__link">
              <i class="icon-note"></i>
            </a>
          </li>

          <li class="sidebar__item">
            <a href="#contact" class="sidebar__link">
              <i class="icon-bubble"></i>
            </a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="sidebar__footer">
      <span class="sidebar__copyright">&copy; 2022 - 2023</span>
    </div>
  </aside>
</template>

<script setup>
import Logo from "../assets/logo.svg";
</script>

<style scoped>
.sidebar {
  position: fixed;
  left: 0;
  top: 0;
  background: var(--body-color);
  border-right: 1px solid rgba(0, 0, 0, 0.05);
  padding: 2.5rem;
  width: 110px;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  z-index: 10;
}

.sidebar__list {
  display: flex;
  flex-direction: column;
  row-gap: 1rem;
}

.sidebar__link {
  font-size: 1.5rem;
  color: var(--title-color);
  font-weight: var(--font-bold);
}

.sidebar__copyright {
  color: hsl(245, 15%, 65%);
  font-size: var(--small-font-size);
  writing-mode: vertical-rl;
  transform: rotate(-180deg);
}
</style>
