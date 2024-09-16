<script setup>
// Tady nemusíš zatím přidávat žádný další kód
</script>

<template>
  <!-- Začátek about -->
  <section id="about" class="section">
    <div class="about-box">
      <div class="about-content">
        <h2>O nás</h2>
        <p>
          V Café Aroma věříme, že káva je víc než jen nápoj – je to zážitek, který spojuje lidi. Naše kavárna s
          dlouholetou tradicí se nachází v srdci města a je místem, kde si můžete vychutnat výběrovou kávu, domácí
          dezerty a příjemnou atmosféru. Všechny naše kávové zrna pečlivě vybíráme od malých, rodinných farem z celého
          světa, abychom zajistili tu nejvyšší kvalitu a jedinečnou chuť.
        </p>
        <p>
          Každý šálek kávy připravujeme s láskou a respektem k tradičním metodám pražení a přípravy. Nezáleží na tom,
          zda preferujete klasické espresso, jemné latte, nebo chcete vyzkoušet náš podpisový nápoj – v Café Aroma
          vždy najdete něco, co potěší vaše chuťové buňky.
        </p>
        <p>
          Kromě výběrové kávy nabízíme i široký výběr domácích dezertů, které denně připravuje náš zkušený tým cukrářů.
          Ať už je to lahodný čokoládový dort, lehký cheesecake, nebo tradiční croissant, všechny naše sladkosti jsou
          vyráběny s důrazem na čerstvost a kvalitu surovin.
        </p>
        <p>
          Přijďte si k nám odpočinout, načerpat energii nebo strávit příjemný čas s přáteli či rodinou. Těšíme se, že
          vás brzy přivítáme v Café Aroma, kde se káva a přátelská atmosféra setkávají v dokonalé harmonii.
        </p>
      </div>
    </div>
  </section>
  <!-- Konec about -->
</template>

<style scoped>
/* Začátek about */
#about {
  text-align: center;
  background-image: url("../../assets/images/interior.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover; /* Pro zajištění, že obrázek pokryje celý background */
  width: 100%;
  height: 95vh;
}

.about-box {
  background-color: rgba(0, 0, 0, 0.7);
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.about-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 30px;
  border: 2px solid white;
  max-width: 50%; /* Na větších obrazovkách bude obsah maximálně 50% šířky */
  padding: 25px;
  border-radius: 10px;
  background-color: rgba(0, 0, 0, 0.7);
}

.about-content h2 {
  font-size: 2.5rem;
  color: #c46a2a;
}

.about-content p {
  font-size: 18px;
  color: white;
}

/* Responzivní design pro menší obrazovky */
@media (max-width: 768px) {
  .about-content {
    max-width: 80%; /* Na tabletech a menších zařízeních zabere až 80% šířky */
  }

  .about-content h2 {
    font-size: 2rem; /* Zmenšení fontu pro nadpisy na menších zařízeních */
  }

  .about-content p {
    font-size: 16px; /* Zmenšení velikosti textu na menších zařízeních */
  }
}

@media (max-width: 480px) {
  #about {
    height: auto; /* Umožňuje vyšším mobilním zařízením roztáhnout výšku */
    padding: 20px 0; /* Upravíme padding pro mobilní zařízení */
  }

  .about-content {
    max-width: 95%; /* Na mobilních zařízeních zabere až 95% šířky */
  }

  .about-content h2 {
    font-size: 1.8rem; /* Dále zmenšíme nadpis pro lepší čitelnost */
  }

  .about-content p {
    font-size: 14px; /* Zmenšíme font velikost pro lepší zobrazení na mobilech */
  }
}
/* Konec about */
</style>
