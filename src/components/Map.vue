<template>
    <section class="section">
        <div class="container">
            <h2>Где нас найти</h2>
            <div class="map-container">
                <iframe
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2923.781377252976!2d38.97195321557965!3d45.03547247905617!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x40f0c5b3b5c6b5b5%3A0x7b5f5f5f5f5f5f5!2z0JzQvtGB0LrQstCw!5e0!3m2!1sru!2sru!4v1640000000000!5m2!1sen!2sru"
                    width="100%" height="400" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Map'
}
</script>

<style scoped>
.map-container {
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

.map-container iframe {
    border: none;
}
</style>
