<template>
  <!-- Začátek menu -->
  <section id="menu" class="section">
    <div class="menu-section">
      <h2>Naše menu</h2>

      <!-- Kategorie: Káva -->
      <div class="menu-category">
        <h3>Káva</h3>
        <div class="menu-items">
          <div class="menu-item">
            <h4>Espresso</h4>
            <p>Silná a bohatá chuť</p>
            <span class="price">50 Kč</span>
          </div>
          <div class="menu-item">
            <h4>Latte Macchiato</h4>
            <p>Jemné latte s bohatou mléčnou pěnou</p>
            <span class="price">75 Kč</span>
          </div>
          <div class="menu-item">
            <h4>Cappuccino</h4>
            <p>Krémová chuť s horkým mlékem</p>
            <span class="price">70 Kč</span>
          </div>
        </div>
      </div>

      <!-- Kategorie: Dezerty -->
      <div class="menu-category">
        <h3>Dezerty</h3>
        <div class="menu-items">
          <div class="menu-item">
            <h4>Domácí čokoládový dort</h4>
            <p>Vyroben z kvalitní čokolády a čerstvých ingrediencí</p>
            <span class="price">90 Kč</span>
          </div>
          <div class="menu-item">
            <h4>Cheesecake</h4>
            <p>Lehký a krémový s nádechem citronu</p>
            <span class="price">85 Kč</span>
          </div>
          <div class="menu-item">
            <h4>Francouzský croissant</h4>
            <p>Křupavý a máslový croissant</p>
            <span class="price">45 Kč</span>
          </div>
        </div>
      </div>

      <!-- Speciální nabídka -->
      <div class="menu-category">
        <h3>Speciální nabídka</h3>
        <div class="menu-items">
          <div class="menu-item">
            <h4>Ledová káva</h4>
            <p>Osvěžující a lahodná, ideální na horké dny</p>
            <span class="price">80 Kč</span>
          </div>
          <div class="menu-item">
            <h4>Horká čokoláda</h4>
            <p>Bohatá a krémová čokoláda, ideální na zahřátí</p>
            <span class="price">75 Kč</span>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- Konec menu -->
</template>

<style scoped>
/* Začátek menu */
#menu {
  background-image: url('../../assets/images/menu.jpg');
  background-position: center;
  background-size: cover;
}

.menu-section {
  padding: 60px 20px;
  background-color: rgba(0, 0, 0, 0.7);
  width: 100%;
  height: 100%;
}

.menu-section h2 {
  text-align: center;
  color: #c46a2a;
  font-size: 2.5rem;
}

.menu-category {
  margin: 40px 0;
  text-align: center;
}

.menu-category h3 {
  color: #419156;
  font-size: 2rem;
  margin-bottom: 20px;
}

.menu-items {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}

.menu-item {
  background-color: #f8f8f8;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  flex: 1 1 calc(33.333% - 20px);
  max-width: 300px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.menu-item h4 {
  margin: 0 0 10px;
  color: #333;
}

.menu-item p {
  margin: 0 0 10px;
  font-size: 0.9rem;
  color: #666;
  text-align: center;
}

.menu-item .price {
  color: #6F4E37;
  font-weight: bold;
  font-size: 1.1rem;
}

/* Responzivní stylování */

/* Pro tablety a menší obrazovky */
@media (max-width: 768px) {
  .menu-item {
    flex: 1 1 calc(50% - 20px); /* Dvě položky vedle sebe na tabletech */
  }
}

/* Pro mobilní telefony */
@media (max-width: 480px) {
  .menu-item {
    flex: 1 1 100%; /* Jedna položka na řádek na mobilních telefonech */
    max-width: 100%;
  }

  .menu-section h2 {
    font-size: 2rem;
  }

  .menu-category h3 {
    font-size: 1.8rem;
  }

  .menu-item h4 {
    font-size: 1.2rem;
  }

  .menu-item p {
    font-size: 0.85rem;
  }

  .menu-item .price {
    font-size: 1rem;
  }
}
/* Konec menu */
</style>
