<template>
    <section id="about" class="section">
        <div class="container">
            <h2>Обо мне</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Меня зовут Анна Петрова, я — сертифицированный агент по недвижимости с 12‑летним опытом работы.
                        Специализируюсь на жилой недвижимости в Краснодаре и окрестностях.</p>
                    <p>Мой подход — индивидуальный подбор вариантов с учётом ваших пожеланий и бюджета. Я сопровождаю
                        сделку от первого звонка до подписания договора.</p>
                </div>
                <div class="about-stats">
                    <div class="stat-item">
                        <span class="stat-number">150+</span>
                        <span class="stat-label">Успешных сделок</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">12</span>
                        <span class="stat-label">Лет опыта</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">98%</span>
                        <span class="stat-label">Довольных клиентов</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'About'
}
</script>

<style scoped>
.section {
    padding: 80px 0;
}

.section h2 {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 3rem;
    color: var(--copper);
}

.about-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
}

.about-text p {
    margin-bottom: 1.5rem;
    font-size: 1.1rem;
}

.about-stats {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    text-align: center;
}

.stat-item {
    padding: 20px;
}

.stat-number {
    display: block;
    font-size: 2.5rem;
    font-weight: bold;
    color: var(--copper);
}

.stat-label {
    font-size: 0.9rem;
    opacity: 0.8;
}

@media (max-width: 768px) {
    .about-content {
        grid-template-columns: 1fr;
        gap: 2rem;
    }

    .section h2 {
        font-size: 2rem;
    }
}
</style>
