<template>
    <footer class="footer">
        <div class="footer-container">
            <!-- Logo nebo název kavárny -->
            <div class="footer-brand">
                <h3>Café Aroma</h3>
            </div>

            <!-- Navigační odkazy -->
            <div class="footer-nav">
                <ul>
                    <li><a href="#hero" @click.prevent="scrollToSection('hero')">Home</a></li>
                    <li><a href="#menu" @click.prevent="scrollToSection('menu')">Menu</a></li>
                    <li><a href="#about" @click.prevent="scrollToSection('about')">About</a></li>
                    <li><a href="#contact" @click.prevent="scrollToSection('contact')">Contact</a></li>
                </ul>
            </div>

            <!-- Sociální média -->
            <div class="footer-social">
                <h4>Follow us</h4>
                <ul class="social-links">
                    <li><a href="#"><font-awesome-icon :icon="['fab', 'facebook']" /></a></li>
                    <li><a href="#"><font-awesome-icon :icon="['fab', 'instagram']" /></a></li>
                </ul>
            </div>

            <!-- Kontaktní informace -->
            <div class="footer-contact">
                <h4>Contact</h4>
                <p><font-awesome-icon :icon="['fas', 'map-pin']" /> Hlavní ulice 123, Praha</p>
                <p><font-awesome-icon :icon="['fas', 'phone']" /> +420 123 456 789</p>
                <p><font-awesome-icon :icon="['fas', 'envelope']" /> info@cafearoma.cz</p>
            </div>
        </div>

        <!-- Copyright -->
        <div class="footer-bottom">
            <p>&copy; 2024 Café Aroma.</p>
        </div>
    </footer>
</template>

<script setup>

function scrollToSection(id) {
    const section = document.getElementById(id);
    if (section) {
        window.scrollTo({
            top: section.offsetTop - 50,  // 50px offset kvůli pevné navigaci
            behavior: 'smooth'            // Plynulé scrollování
        });
    }
}

</script>

<style scoped>
/* Footer hlavní stylování */
.footer {
    background-color: #6f4e37;
    color: white;
    padding: 40px 20px;
    text-align: center;
}

.footer-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 20px;
    max-width: 1200px;
    margin: 0 auto;
}

/* Stylování značky */
.footer-brand h3 {
    font-size: 1.8rem;
    color: #fff;
    text-transform: uppercase;
}

/* Navigační odkazy */
.footer-nav ul {
    list-style: none;
    padding: 0;
}

.footer-nav ul li {
    margin-bottom: 10px;
}

.footer-nav ul li a {
    color: #fff;
    text-decoration: none;
    transition: color 0.3s;
}

.footer-nav ul li a:hover {
    color: #c46a2a;
}

/* Sociální média */

.footer-social ul {
    list-style: none;
}

.footer-social h4 {
    color: #fff;
    margin-bottom: 10px;
}

.footer-social .social-links {
    display: flex;
    justify-content: center;
    gap: 15px;
}

.footer-social .social-links li a {
    color: #fff;
    font-size: 1.5rem;
    transition: color 0.3s;
}

.footer-social .social-links li a:hover {
    color: #c46a2a;
}

/* Kontaktní informace */
.footer-contact h4 {
    color: #fff;
    margin-bottom: 10px;
}

.footer-contact p {
    margin: 0;
    margin-bottom: 10px;
    font-size: 0.9rem;
    color: #fff;
}

.footer-contact p svg {
    margin-right: 10px;
}

/* Copyright */
.footer-bottom {
    background-color: #5a3c2b;
    padding: 10px 0;
    margin-top: 20px;
    font-size: 0.9rem;
}

.footer-bottom p {
    margin: 0;
}

/* Responzivní stylování */
@media (max-width: 768px) {
    .footer-container {
        flex-direction: column;
        align-items: center;
    }

    .footer-nav ul,
    .footer-social .social-links {
        display: flex;
        justify-content: center;
        gap: 15px;
    }
}
</style>