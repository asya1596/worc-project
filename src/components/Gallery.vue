<template>
    <section id="gallery" class="section bg-dark">
        <div class="container">
            <h2>Галерея объектов</h2>
            <div class="gallery-grid">
                <div class="gallery-item" data-src="https://picsum.photos/600/400?random=1">
                    <img src="https://picsum.photos/300/200?random=1" alt="Квартира в новостройке">
                    <div class="overlay">Посмотреть</div>
                </div>
                <div class="gallery-item" data-src="https://picsum.photos/600/400?random=2">
                    <img src="https://picsum.photos/300/200?random=2" alt="Дом в пригороде">
                    <div class="overlay">Посмотреть</div>
                </div>
                <div class="gallery-item" data-src="https://picsum.photos/600/400?random=3">
                    <img src="https://picsum.photos/300/200?random=3" alt="Коммерческая недвижимость">
                    <div class="overlay">Посмотреть</div>
                </div>
                <div class="gallery-item" data-src="https://picsum.photos/600/400?random=4">
                    <img src="https://picsum.photos/300/200?random=4" alt="Апартаменты у моря">
                    <div class="overlay">Посмотреть</div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Gallery'
}
</script>

<style scoped>
.gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1rem;
}

.gallery-item {
    position: relative;
    overflow: hidden;
    border-radius: 8px;
    cursor: pointer;
}

.gallery-item img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    transition: var(--transition);
}

.overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(184, 115, 51, 0.8);
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-weight: bold;
    opacity: 0;
    transition: var(--transition);
}

.gallery-item:hover .overlay {
    opacity: 1;
}

.gallery-item:hover img {
    transform: scale(1.1);
}

@media (max-width: 768px) {
    .gallery-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 480px) {
    .gallery-grid {
        grid-template-columns: 1fr;
    }
}
</style>
