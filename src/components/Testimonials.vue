<template>
    <section id="testimonials" class="section bg-dark">
        <div class="container">
            <h2>Отзывы клиентов</h2>
            <div class="testimonials-grid">
                <div class="testimonial-card">
                    <div class="quote-icon">“</div>
                    <p class="testimonial-text">Анна помогла нам найти идеальную квартиру в новостройке. Всё сделала
                        быстро и профессионально, учла все наши пожелания. Очень довольны результатом!</p>
                    <div class="testimonial-author">— Мария Сидорова</div>
                </div>
                <div class="testimonial-card">
                    <div class="quote-icon">“</div>
                    <p class="testimonial-text">Продавал квартиру через Анну. Она организовала показы, провела
                        переговоры и довела сделку до конца. Очень грамотный специалист!</p>
                    <div class="testimonial-author">— Алексей Иванов</div>
                </div>
                <div class="testimonial-card">
                    <div class="quote-icon">“</div>
                    <p class="testimonial-text">Профессионал своего дела! Нашла подходящий вариант аренды за 3 дня.
                        Рекомендую Анну как ответственного и внимательного агента.</p>
                    <div class="testimonial-author">— Екатерина Петрова</div>
                </div>
                <div class="testimonial-card">
                    <div class="quote-icon">“</div>
                    <p class="testimonial-text">Работали с Анной при покупке дома. Поразила её внимательность к деталям
                        и знание рынка недвижимости. Сделка прошла гладко.</p>
                    <div class="testimonial-author">— Дмитрий Николаев</div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Testimonials'
}
</script>

<style scoped>
.bg-dark {
    background: var(--dark-card);
}

.testimonials-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
}

.testimonial-card {
    background: var(--graphite);
    padding: 2rem;
    border-radius: 8px;
    transition: var(--transition);
    border-left: 4px solid var(--copper);
    position: relative;
    overflow: hidden;
}

.testimonial-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
}

.quote-icon {
    font-size: 4rem;
    color: var(--copper);
    opacity: 0.3;
    position: absolute;
    top: 10px;
    right: 15px;
    line-height: 1;
}

.testimonial-text {
    margin-bottom: 1.5rem;
    font-style: italic;
    line-height: 1.6;
    position: relative;
    z-index: 1;
}

.testimonial-author {
    color: var(--cream);
    font-weight: bold;
    text-align: right;
    position: relative;
    z-index: 1;
}

/* Адаптивность для планшетов */
@media (max-width: 1024px) {
    .testimonials-grid {
        grid-template-columns: repeat(2, 1fr);
        gap: 1.5rem;
    }
}

/* Адаптивность для мобильных устройств */
@media (max-width: 768px) {
    .testimonials-grid {
        grid-template-columns: 1fr;
        gap: 1rem;
    }

    .testimonial-card {
        padding: 1.5rem;
    }

    .quote-icon {
        font-size: 3rem;
    }

    .testimonial-text {
        font-size: 1rem;
    }
}

/* Для очень маленьких экранов */
@media (max-width: 480px) {
    .testimonial-card {
        padding: 1rem;
    }

    .testimonial-text {
        font-size: 0.9rem;
        margin-bottom: 1rem;
    }

    .testimonial-author {
        font-size: 0.9rem;
    }

    .quote-icon {
        display: none;
    }
}
</style>
