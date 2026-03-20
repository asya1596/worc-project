<template>
    <nav class="navbar">
        <div class="nav-container">
            <a href="#" class="logo">Агент недвижимости</a>
            <button class="hamburger" id="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </button>
            <ul class="nav-menu" id="navMenu">
                <li><a href="#home">Главная</a></li>
                <li><a href="#about">Обо мне</a></li>
                <li><a href="#services">Услуги</a></li>
                <li><a href="#testimonials">Отзывы</a></li>
                <li><a href="#gallery">Галерея</a></li>
                <li><a href="#contact">Контакты</a></li>
            </ul>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped>
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background: rgba(28, 28, 30, 0.95);
    backdrop-filter: blur(10px);
    z-index: 1000;
    padding: 1rem 0;
    border-bottom: 1px solid var(--copper);
}

.nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.logo {
    font-size: 1.5rem;
    font-weight: bold;
    color: var(--copper);
    text-decoration: none;
}

.nav-menu {
    display: flex;
    list-style: none;
    gap: 2rem;
}

.nav-menu a {
    color: var(--cream);
    text-decoration: none;
    transition: var(--transition);
    position: relative;
}

.nav-menu a:hover {
    color: var(--copper);
}

.nav-menu a::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 0;
    height: 2px;
    background: var(--copper);
    transition: var(--transition);
}

.nav-menu a:hover::after {
    width: 100%;
}

.hamburger {
    display: none;
    flex-direction: column;
    cursor: pointer;
    border: none;
    background: none;
    padding: 5px;
}

.hamburger span {
    display: block;
    width: 25px;
    height: 3px;
    background: var(--copper);
    margin: 4px 0;
    transition: var(--transition);
}

@media (max-width: 768px) {
    .nav-menu {
        position: fixed;
        top: 70px;
        left: 0;
        width: 100%;
        background: var(--graphite);
        flex-direction: column;
        padding: 20px 0;
        display: none;
    }

    .nav-menu.active {
        display: flex;
    }

    .hamburger {
        display: flex;
    }
}
</style>
