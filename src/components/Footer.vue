<template>
    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-section">
                    <h3>Агент недвижимости</h3>
                    <p>Подберём недвижимость под ваши запросы. Профессиональная помощь в покупке, продаже и аренде
                        жилья.</p>
                </div>
                <div class="footer-section">
                    <h3>Быстрые ссылки</h3>
                    <ul>
                        <li><a href="#home">Главная</a></li>
                        <li><a href="#about">Обо мне</a></li>
                        <li><a href="#services">Услуги</a></li>
                        <li><a href="#testimonials">Отзывы</a></li>
                        <li><a href="#gallery">Галерея</a></li>
                        <li><a href="#contact">Контакты</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Контакты</h3>
                    <ul>
                        <li>г. Краснодар, ул. Ленина, 123</li>
                        <li>+7 (999) 123-45-67</li>
                        <li>info@realestate.ru</li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Соцсети</h3>
                    <div class="social-links">
                        <a href="#" aria-label="ВКонтакте"><i>VK</i></a>
                        <a href="#" aria-label="Telegram"><i>TG</i></a>
                        <a href="#" aria-label="WhatsApp"><i>WA</i></a>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 Агент недвижимости. Все права защищены.</p>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style scoped>
.footer {
    background: var(--dark-card);
    padding: 60px 0 30px;
    color: var(--cream);
}

.footer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 3rem;
    margin-bottom: 40px;
}

.footer-section h3 {
    color: var(--copper);
    margin-bottom: 1.5rem;
    font-size: 1.2rem;
}

.footer-section ul {
    list-style: none;
}

.footer-section li,
.footer-section p {
    margin-bottom: 0.8rem;
}

.footer-section a {
    color: var(--cream);
    text-decoration: none;
    transition: var(--transition);
}

.footer-section a:hover {
    color: var(--copper);
}

.social-links {
    display: flex;
    gap: 1rem;
}

.social-links a {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    background: rgba(184, 115, 51, 0.2);
    border-radius: 50%;
    transition: var(--transition);
}

.social-links a:hover {
    background: var(--copper);
    transform: translateY(-2px);
}

.footer-bottom {
    text-align: center;
    padding-top: 30px;
    border-top: 1px solid #444;
    color: #aaa;
}

@media (max-width: 768px) {
    .footer-grid {
        grid-template-columns: 1fr;
        gap: 2rem;
    }
}
</style>
