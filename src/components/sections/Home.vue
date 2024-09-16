<template>
  <section id="hero" class="section">
    <div class="hero-content">
      <h1>Vítejte v <a style="color: #c46a2a;">Café Aroma</a></h1>
      <a href="#menu" @click.prevent="scrollToSection('menu')" class="btn-primary">ZOBRAZIT MENU</a>
    </div>
  </section>
</template>

<script setup>
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
html {
  scroll-behavior: smooth;
}

/* Hero sekce */
#hero {
  background-image: url('../../assets/images/hero-photo.jpeg');
  background-size: cover;
  background-position: center;
  height: 95vh;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  text-align: center;
  width: 100%;
}

.hero-content {
  background-color: rgba(0, 0, 0, 0.7);
  padding: 20px;
  border-radius: 10px;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.hero-content h1 {
  font-size: 2.5rem;
  margin-bottom: 40px;
}

.hero-content p {
  max-width: 30%;
  padding: 40px 0;
}

.btn-primary {
  background-color: #6F4E37;
  color: white;
  padding: 10px 20px;
  text-decoration: none;
  font-weight: bold;
  border-radius: 5px;
  transition: background-color 0.3s;
}

.btn-primary:hover {
  background-color: #419156;
}

/* Responzivní stylování */

/* Pro tablety a menší obrazovky */
@media (max-width: 768px) {

  .hero-content h1 {
    font-size: 2rem;
  }

  .btn-primary {
    padding: 10px 15px;
  }
}

/* Pro mobilní telefony */
@media (max-width: 480px) {

  .hero-content h1 {
    font-size: 1.8rem;
  }

  .btn-primary {
    padding: 8px 12px;
    font-size: 0.95rem;
  }
}
</style>
