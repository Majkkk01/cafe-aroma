<template>
  <nav>
    <div class="logo">
      <a href="#hero" @click.prevent="scrollToSection('hero')">Café Aroma</a>
    </div>

    <!-- Hamburger menu pro malé obrazovky -->
    <div class="menu-toggle" @click="toggleMenu">
      <font-awesome-icon :icon="['fas', 'bars']" />
    </div>

    <ul :class="{ 'nav-active': isActive }">
      <li><a href="#hero" @click.prevent="scrollToSection('hero')" class="nav-item">Home</a></li>
      <li><a href="#menu" @click.prevent="scrollToSection('menu')" class="nav-item">Menu</a></li>
      <li><a href="#about" @click.prevent="scrollToSection('about')" class="nav-item">About</a></li>
      <li><a href="#contact" @click.prevent="scrollToSection('contact')" class="nav-item">Contact</a></li>
    </ul>

    <div id="social-nav">
      <ul class="social-links">
        <li><a href="#"><font-awesome-icon :icon="['fab', 'facebook']" class="social-icon" /></a></li>
        <li><a href="#"><font-awesome-icon :icon="['fab', 'instagram']" class="social-icon" /></a></li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue';

// Toggle pro mobilní menu
const isActive = ref(false);

function toggleMenu() {
  isActive.value = !isActive.value;
}

function scrollToSection(id) {
  const section = document.getElementById(id);
  if (section) {
    window.scrollTo({
      top: section.offsetTop - 50, // 50px offset kvůli pevné navigaci
      behavior: 'smooth', // Plynulé scrollování
    });
  }
}
</script>

<style scoped>
/* Základní styl pro navbar */
nav {
  background-color: #6f4e37;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 70px;
  padding: 20px 50px;
  position: fixed;
  top: 0;
  z-index: 100;
}

/* Styl pro logo */
.logo a {
  color: white;
  text-decoration: none;
  font-size: 1.5rem;
  font-family: 'Playfair Display', system-ui;
  font-weight: 500;
}

/* Základní styl pro navigační odkazy */
nav ul {
  list-style-type: none;
  display: flex;
  justify-content: center;
  margin: 0;
}

nav li {
  padding: 5px;
  font-size: 1.5rem;
  color: white;
  text-transform: uppercase;
  font-family: 'Playfair Display', system-ui;
}

.nav-item {
  color: white;
  text-decoration: none;
  font-weight: bold;
  position: relative;
  transition: color 0.3s ease, transform 0.3s ease;
}

.nav-item:hover {
  color: #419156;
  transform: translateY(-2px);
}

.nav-item::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -5px;
  width: 0;
  height: 2px;
  background-color: #419156;
  transition: width 0.3s ease;
}

.nav-item:hover::after {
  width: 100%;
}

/* Styl pro sociální odkazy */
#social-nav {
  display: flex;
}

.social-links {
  display: flex;
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.social-icon {
  color: white;
  font-size: 1.5rem;
  padding: 10px;
  border-radius: 50%;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

.social-icon:hover {
  background-color: #419156;
  transform: scale(1.1);
}

/* Skrytí menu pro malé obrazovky */
.menu-toggle {
  display: none;
  font-size: 2rem;
  color: white;
  cursor: pointer;
}

/* Styl pro aktivní stav menu (mobilní verze) */
.nav-active {
  display: block;
}

@media (max-width: 768px) {
  /* Hamburger menu */
  .menu-toggle {
    display: block;
  }

  /* Skrytí navigačních odkazů v defaultu pro malé obrazovky */
  nav ul {
    position: absolute;
    top: 70px;
    right: 0;
    height: 100vh;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.95);
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    padding-top: 50px;
    display: none;
  }

  nav ul li {
    margin: 20px 0;
  }

  /* Styl pro zobrazení navigace po kliknutí na hamburger menu */
  .nav-active {
    display: flex;
  }

  /* Skrytí sociálních ikon v mobilní verzi (pokud chceš) */
  #social-nav {
    display: none;
  }
}
</style>
