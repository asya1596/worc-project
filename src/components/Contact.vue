<template>
    <section id="contact" class="section">
        <div class="container">
            <h2>Свяжитесь со мной</h2>
            <form class="contact-form" id="contactForm">
                <div class="form-group">
                    <label for="name">Имя *</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email *</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="phone">Телефон</label>
                    <input type="tel" id="phone" name="phone">
                </div>
                <div class="form-group">
                    <label for="message">Сообщение *</label>
                    <textarea id="message" name="message" rows="5" required></textarea>
                </div>
                <button type="submit" class="btn">Отправить сообщение</button>
            </form>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Contact'
}
</script>

<style scoped>
.contact-form {
    max-width: 600px;
    margin: 0 auto;
}

.form-group {
    margin-bottom: 1.5rem;
}

label {
    display: block;
    margin-bottom: 0.5rem;
    color: var(--copper);
}

input,
textarea {
    width: 100%;
    padding: 12px;
    background: var(--dark-card);
    border: 1px solid #444;
    border-radius: 4px;
    color: var(--cream);
    font-size: 1rem;
    transition: var(--transition);
}

input:focus,
textarea:focus {
    outline: none;
    border-color: var(--copper);
    box-shadow: 0 0 0 2px rgba(184, 115, 51, 0.3);
}

button[type="submit"] {
    background: var(--copper);
    color: var(--graphite);
    padding: 12px 30px;
    border: none;
    border-radius: 4px;
    font-weight: bold;
    cursor: pointer;
    transition: var(--transition);
}

button[type="submit"]:hover {
    background: #d48a4a;
}
</style>
