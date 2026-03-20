<template>
    <section id="services" class="section bg-dark">
        <div class="container">
            <h2>Мои услуги</h2>
            <div class="services-grid">
                <div class="service-card">
                    <h3>Покупка жилья</h3>
                    <p>Подбор квартир и домов с учётом вашего бюджета и пожеланий. Проверка юридической чистоты.</p>
                </div>
                <div class="service-card">
                    <h3>Продажа недвижимости</h3>
                    <p>Оценка рыночной стоимости, профессиональная фотосъёмка, продвижение объекта.</p>
                </div>
                <div class="service-card">
                    <h3>Аренда жилья</h3>
                    <p>Поиск арендаторов или подходящих вариантов для аренды на любой срок.</p>
                </div>
                <div class="service-card">
                    <h3>Сопровождение сделок</h3>
                    <p>Юридическое сопровождение на всех этапах: от договора до регистрации в Росреестре.</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Services'
}
</script>

<style scoped>
.bg-dark {
    background: var(--dark-card);
}

.services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
}

.service-card {
    background: var(--dark-card);
    padding: 2rem;
    border-radius: 8px;
    text-align: center;
    transition: var(--transition);
    border-left: 4px solid var(--copper);
}

.service-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
}

.service-card h3 {
    color: var(--copper);
    margin-bottom: 1rem;
}

@media (max-width: 768px) {
    .services-grid {
        grid-template-columns: 1fr;
    }
}
</style>
