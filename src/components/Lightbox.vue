<template>
    <div class="lightbox" v-if="isOpen" @click.self="close">
        <button class="lightbox-close" @click="close">×</button>
        <img :src="currentImage" alt="Увеличенное изображение">
    </div>
</template>

<script>
export default {
    name: 'Lightbox',
    data() {
        return {
            isOpen: false,
            currentImage: ''
        };
    },
    methods: {
        open(imageUrl) {
            this.currentImage = imageUrl;
            this.isOpen = true;
            document.body.style.overflow = 'hidden';
        },
        close() {
            this.isOpen = false;
            document.body.style.overflow = 'auto';
        }
    },
    created() {
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape' && this.isOpen) {
                this.close();
            }
        });
    }
};
</script>

<style scoped>
.lightbox {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.9);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 9999;
}

.lightbox img {
    max-width: 90%;
    max-height: 90%;
    border-radius: 4px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
}

.lightbox-close {
    position: absolute;
    top: 20px;
    right: 20px;
    background: none;
    border: none;
    color: white;
    font-size: 3rem;
    cursor: pointer;
}
</style>
