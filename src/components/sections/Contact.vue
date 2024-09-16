<template>
  <section id="contact" class="section">
    <div class="contact-section">
      <h2>Kontaktujte nás</h2>
      <h3>Máte otázky? Napište nám!</h3>
      <div class="form-box">
        <div class="contact-form">
          <form @submit.prevent="handleSubmit">
            <input type="text" id="name" v-model="name" placeholder="Name" required />
            <input type="email" id="email" v-model="email" placeholder="Email" required />
            <textarea id="message" v-model="message" placeholder="Message" required></textarea>
            <button type="submit" class="btn-primary">Odeslat</button>
          </form>
        </div>
        <div class="contact-info">
          <div class="contact-column">
            <div class="address relas-center">
              <h4><font-awesome-icon :icon="['fas', 'map-pin']" /> Adresa</h4>
              <p>ADDRESS 01/25</p>
            </div>
            <div class="email-phone relas-center">
              <h4><font-awesome-icon :icon="['fas', 'address-book']" />Kontakt</h4>
              <p>+420 123 456 789</p>
              <p>email@email.cz</p>
            </div>
            <div class="open-close relas-center">
              <h4><font-awesome-icon :icon="['fas', 'clock']" />Otevírací doba</h4>
              <p>Po-Pá: 8-19</p>
              <p>So-Ne: 10-17</p>
            </div>
          </div>
        </div>
      </div>
      <!-- Mapa -->
      <div class="map">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2564.896473125209!2d14.420668915715644!3d50.07649827942656!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x470b94e877a9ad69%3A0xa00c3a10557f9712!2sOld%20Town%20Square!5e0!3m2!1sen!2scz!4v1631793938389!5m2!1sen!2scz"
          width="100%"
          height="300"
          style="border:0;"
          allowfullscreen=""
          loading="lazy"
        ></iframe>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

// Základní stavy pro formulářová pole
const name = ref('');
const email = ref('');
const message = ref('');

// Funkce pro zpracování formuláře (zatím jen výpis do konzole)
const handleSubmit = () => {
  console.log(`Name: ${name.value}, Email: ${email.value}, Message: ${message.value}`);
};
</script>

<style scoped>
/* Globální styl pro kontaktní sekci */
#contact {
  position: relative;
  background-image: url("../../assets/images/contact.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  padding: 60px 20px;
  z-index: 1;
}

/* Překryv (overlay) pro zatmavení obrázku */
#contact::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7); /* Tmavý překryv */
  z-index: -1; /* Zajišťuje, že překryv bude pod obsahem sekce */
}

.contact-section {
  position: relative;
  z-index: 2;
  padding: 40px 20px;
  border-radius: 10px;
  max-width: 1200px;
  margin: 0 auto;
  background-color: rgba(255, 255, 255, 0.8); /* Jemné pozadí pro lepší čitelnost */
}

.contact-section h2 {
  color: #c46a2a;
  font-size: 2.5rem;
  margin-bottom: 20px;
  text-align: center;
}

.contact-section h3 {
  color: #419156;
  font-size: 1.8rem;
  margin-bottom: 40px;
  text-align: center;
}

/* Form-box pro lepší rozdělení a centrování */
.form-box {
  display: flex;
  justify-content: space-between; /* Položí form a contact-info na dvě půlky */
  align-items: center; /* Vycentruje obsah vertikálně */
  padding: 40px;
  border: 2px solid #c46a2a;
  border-radius: 10px;
  background-color: rgba(255, 255, 255, 0.9);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  gap: 20px; /* Mezera mezi form a contact-info */
}

/* Nastavení form-boxu, aby každý element měl 50% šířku */
.contact-form,
.contact-info {
  flex: 1; /* Zajistí rovnoměrné rozložení prostoru */
  max-width: 50%; /* Zajistí, že každý bude mít 50% šířky */
}

.contact-form form {
  display: flex;
  flex-direction: column;
}

.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 15px;
  margin-bottom: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  font-size: 16px;
}

.contact-form textarea {
  height: 150px;
  resize: none;
}

.contact-form .btn-primary {
  background-color: #6f4e37;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-weight: 700;
  text-transform: uppercase;
  transition: background-color 0.3s;
}

.contact-form .btn-primary:hover {
  background-color: #419156;
}

.contact-column {
  padding: 0 100px;
}

.contact-column h4 {
  font-size: 1.5rem;
  text-transform: uppercase;
  color: #419156;
  margin-bottom: 10px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.contact-column p {
  color: #333;
  margin-bottom: 20px;
  font-size: 1.1rem;
}

/* Mapa */
.map {
  margin-top: 40px;
}

.map iframe {
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* Responzivní stylování */
@media (max-width: 768px) {
  .form-box {
    flex-direction: column;
    padding: 20px;
  }

  .contact-column {
  padding: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}

.contact-column h4 {
  font-size: 1.2rem;
  text-align: center;
}

.contact-column p {
  font-size: 0.8rem;
}

.relas-center {
  text-align: center;
}

  .contact-form,
  .contact-info {
    max-width: 100%; /* Na menších obrazovkách bude každý prvek zabírat 100% šířky */
  }
}

@media (max-width: 480px) {
  .contact-section h2 {
    font-size: 2rem;
  }

  .contact-section h3 {
    font-size: 1.5rem;
  }

  form input,
  form textarea {
    padding: 10px;
  }

  .contact-column {
  padding: 0;
}

  .form-box {
    padding: 20px;
  }

  .map iframe {
    height: 250px;
  }
}
</style>
