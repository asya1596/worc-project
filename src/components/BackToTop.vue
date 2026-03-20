<template>
    <button class="back-to-top" id="backToTop" @click="scrollToTop" :class="{ 'visible': isVisible }">
        ↑
    </button>
</template>

<script>
export default {
    name: 'BackToTop',
    data() {
        return {
            isVisible: false
        };
    },
    mounted() {
        window.addEventListener('scroll', this.checkVisibility);
    },
    beforeUnmount() {
        window.removeEventListener('scroll', this.checkVisibility);
    },
    methods: {
        checkVisibility() {
            this.isVisible = window.pageYOffset > 300;
        },
        scrollToTop() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        }
    }
};
</script>

<style scoped>
.back-to-top {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 50px;
    height: 50px;
    background: var(--copper);
    color: var(--graphite);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    font-size: 1.5rem;
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease;
    z-index: 100;
}

.back-to-top.visible {
    opacity: 1;
    visibility: visible;
}

.back-to-top:hover {
    background: #d48a4a;
    transform: translateY(-3px);
}
</style>
