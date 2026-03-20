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
    background: linear-gradient(rgba(28, 28, 30, 0.7), rgba(28, 28, 30, 0.7)),
        url('https://picsum.photos/1920/1080?blur=2') no-repeat center center/cover;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.hero-content h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
    color: var(--cream);
}

.hero-content p {
    font-size: 1.2rem;
    margin-bottom: 2rem;
    max-width: 600px;
}

.btn {
    display: inline-block;
    background: var(--copper);
    color: var(--graphite);
    padding: 12px 30px;
    text-decoration: none;
    border-radius: 4px;
    font-weight: bold;
    transition: var(--transition);
}

.btn:hover {
    background: #d48a4a;
    transform: translateY(-2px);
}

@media (max-width: 768px) {
    .hero-content h1 {
        font-size: 2rem;
    }

    .hero-content p {
        font-size: 1rem;
    }
}
</style>
