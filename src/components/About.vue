<template>
    <section id="about" class="section">
        <div class="container">
            <h2>Обо мне</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Меня зовут Тхагушева Зарема Абрековна, я —  агент по недвижимости с 12‑летним опытом работы.
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
    padding: 60px 0;
    background-color:var(--graphite);;
}

.section h2 {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 2.5rem;
    color: var(--copper, #b87333);
    line-height: 1.2;
}

.about-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    align-items: center;
}

.about-text p {
    margin-bottom: 1.25rem;
    font-size: 1.1rem;
    line-height: 1.6;
    color: var(--cream);
}

.about-stats {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    text-align: center;
}

.stat-item {
    padding: 18px;
    background: var(--dark-card);
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.08);
}

.stat-number {
    display: block;
    font-size: 2.5rem;
    font-weight: bold;
    color: var(--copper, #b87333);
    margin-bottom: 0.5rem;
}

.stat-label {
    font-size: 0.9rem;
    opacity: 0.8;
    display: block;
}

/* Адаптивность для планшетов (768px - 1024px) */
@media (max-width: 1024px) {
    .section {
        padding: 50px 0;
    }
    
    .section h2 {
        font-size: 2.2rem;
        margin-bottom: 2rem;
    }
    
    .about-content {
        gap: 2.5rem;
    }
    
    .about-text p {
        font-size: 1rem;
    }
    
    .stat-number {
        font-size: 2.2rem;
    }
}

/* Адаптивность для мобильных устройств (до 768px) */
@media (max-width: 768px) {
    .section {
        padding: 40px 0;
    }
    
    .section h2 {
        font-size: 1.8rem;
        margin-bottom: 1.5rem;
        text-align: left;
    }
    
    .about-content {
        grid-template-columns: 1fr;
        gap: 2rem;
    }
    
    .about-text p {
        font-size: 1rem;
        line-height: 1.5;
        margin-bottom: 1rem;
    }
    
    .about-stats {
        grid-template-columns: repeat(2, 1fr);
        gap: 0.75rem;
    }
    
    .stat-item {
        padding: 15px;
    }
    
    .stat-number {
        font-size: 1.8rem;
    }
    
    .stat-label {
        font-size: 0.85rem;
    }
}

/* Для очень маленьких экранов (до 480px) */
@media (max-width: 480px) {
    .section {
        padding: 30px 0;
    }
    
    .section h2 {
        font-size: 1.6rem;
        text-align: center;
    }
    
    .about-stats {
        grid-template-columns: 1fr;
        gap: 0.5rem;
    }
    
    .stat-number {
        font-size: 1.6rem;
    }
    
    .stat-label {
        font-size: 0.8rem;
    }
    
    .about-text p {
        font-size: 0.95rem;
        line-height: 1.45;
    }
}

/* Улучшение читаемости на мобильных */
@media (hover: none) and (pointer: coarse) {
    /* Стили для сенсорных устройств */
    .stat-item {
        padding: 20px 15px; /* Увеличенные отступы для удобного тапа */
    }
}
</style>