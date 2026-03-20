<template>
    <nav class="navbar">
        <div class="nav-container">
            <a href="#" class="logo">Агент недвижимости</a>
            <button class="hamburger" id="hamburger" @click="toggleMenu" :aria-expanded="isMenuOpen"
                aria-label="Открыть меню" :class="{ 'active': isMenuOpen }">
                <span></span>
                <span></span>
                <span></span>
            </button>
            <ul class="nav-menu" id="navMenu" :class="{ 'active': isMenuOpen }">
                <li><a href="#home" @click="closeMenu">Главная</a></li>
                <li><a href="#about" @click="closeMenu">Обо мне</a></li>
                <li><a href="#services" @click="closeMenu">Услуги</a></li>
                <li><a href="#testimonials" @click="closeMenu">Отзывы</a></li>
                <li><a href="#gallery" @click="closeMenu">Галерея</a></li>
                <li><a href="#contact" @click="closeMenu">Контакты</a></li>
            </ul>
        </div>
    </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted, watch } from 'vue'

// Реактивное состояние меню
const isMenuOpen = ref(false)

// Методы управления меню
const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
    isMenuOpen.value = false
}

// Эффект блокировки скролла
watch(isMenuOpen, (newState) => {
    document.body.style.overflow = newState ? 'hidden' : 'auto'
})

// Обработчики событий
let clickHandler
let keyHandler

onMounted(() => {
    // Закрываем меню при клике вне его области
    clickHandler = (event) => {
        if (!event.target.closest('.nav-container') && isMenuOpen.value) {
            closeMenu()
        }
    }
    document.addEventListener('click', clickHandler)

    // Закрываем меню по клавише ESC
    keyHandler = (event) => {
        if (event.key === 'Escape' && isMenuOpen.value) {
            closeMenu()
        }
    }
    document.addEventListener('keydown', keyHandler)
})

onUnmounted(() => {
    // Удаляем обработчики событий при уничтожении компонента
    document.removeEventListener('click', clickHandler)
    document.removeEventListener('keydown', keyHandler)
})
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
    transition: all 0.3s ease;
}

/* Анимация для иконок гамбургера при открытии */
.hamburger.active span:nth-child(1) {
    transform: rotate(45deg) translate(5px, 5px);
}

.hamburger.active span:nth-child(2) {
    opacity: 0;
}

.hamburger.active span:nth-child(3) {
    transform: rotate(-45deg) translate(7px, -6px);
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
        z-index: 999;
        max-height: calc(100vh - 70px);
        overflow-y: auto;
        transform: translateY(-100%);
        transition: transform 0.3s ease-in-out;
    }

    .nav-menu.active {
        display: flex;
        transform: translateY(0);
    }

    .hamburger {
        display: flex;
    }

    /* Уменьшаем отступы для мобильных устройств */
    .nav-menu li {
        margin: 10px 0;
    }

    .nav-menu a {
        padding: 8px 20px;
        width: 100%;
        text-align: center;
        font-size: 1.1rem;
    }
}

/* Для очень маленьких экранов */
@media (max-width: 480px) {
    .nav-container {
        padding: 0 15px;
    }

    .logo {
        font-size: 1.3rem;
    }

    .nav-menu a {
        font-size: 1rem;
        padding: 6px 15px;
    }
}
</style>
