<template>
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Подберём недвижимость под ваши запросы</h1>
            <p>Профессиональный подход к поиску жилья. Более 10 лет опыта на рынке недвижимости.</p>
            <a href="#contact" class="btn">Связаться со мной</a>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Hero'
}
</script>

<style scoped>
.hero {
    height: 100vh;
    min-height: 500px;
    background: linear-gradient(rgba(28, 28, 30, 0.7), rgba(28, 28, 30, 0.7)),
        url('https://picsum.photos/1920/1080?blur=2') no-repeat center center/cover;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 0 20px;
}

.hero-content {
    max-width: 800px;
    width: 100%;
}

.hero-content h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
    color: var(--cream);
    line-height: 1.1;
}

.hero-content p {
    font-size: 1.2rem;
    margin-bottom: 2rem;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
    line-height: 1.5;
}

.btn {
    display: inline-block;
    background: var(--copper);
    color: var(--graphite);
    padding: 14px 32px;
    text-decoration: none;
    border-radius: 4px;
    font-weight: bold;
    transition: var(--transition);
    font-size: 1.1rem;
    text-align: center;
}

.btn:hover {
    background: #d48a4a;
    transform: translateY(-2px);
}

/* Адаптивность для больших экранов (1200px+) */
@media (min-width: 1200px) {
    .hero-content h1 {
        font-size: 3.5rem;
    }

    .btn {
        padding: 16px 40px;
        font-size: 1.2rem;
    }
}

/* Адаптивность для планшетов (769px - 1199px) */
@media (min-width: 769px) and (max-width: 1199px) {
    .hero {
        height: 90vh;
        padding: 0 15px;
    }

    .hero-content h1 {
        font-size: 2.8rem;
    }

    .hero-content p {
        font-size: 1.1rem;
        max-width: 550px;
    }

    .btn {
        padding: 13px 28px;
        font-size: 1rem;
    }
}

/* Адаптивность для мобильных устройств (до 768px) */
@media (max-width: 768px) {
    .hero {
        height: auto;
        min-height: auto;
        padding: 60px 15px 40px;
        align-items: flex-start;
    }

    .hero-content {
        margin-top: 50px;
    }

    .hero-content h1 {
        font-size: 2rem;
        margin-bottom: 0.8rem;
        line-height: 1.2;
    }

    .hero-content p {
        font-size: 1rem;
        margin-bottom: 1.5rem;
        max-width: 100%;
        line-height: 1.4;
    }

    .btn {
        padding: 12px 24px;
        font-size: 1rem;
        width: 100%;
        max-width: 280px;
    }
}

/* Для очень маленьких экранов (до 480px) */
@media (max-width: 480px) {
    .hero {
        padding: 40px 10px 30px;
    }

    .hero-content {
        margin-top: 30px;
    }

    .hero-content h1 {
        font-size: 1.6rem;
    }

    .hero-content p {
        font-size: 0.95rem;
        margin-bottom: 1.2rem;
    }

    .btn {
        padding: 11px 20px;
        font-size: 0.95rem;
        max-width: 260px;
    }
}

/* Улучшение для портретной ориентации мобильных устройств */
@media (max-width: 768px) and (orientation: portrait) {
    .hero {
        padding-bottom: 30px;
    }
}

/* Оптимизация для устройств с высоким DPI */
@media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
    .hero {
        background-size: auto; /* Предотвращает размытие на Retina-экранах */
    }
}
</style>
