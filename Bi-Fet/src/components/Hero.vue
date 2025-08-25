<template>
    <section class="hero-wrapper">
        <img src="../assets/images/hero-background.svg"
            alt="Céu estrelado noturno com pequenas partículas flutuantes, criando um fundo mágico e tecnológico."
            class="hero-background">
        <div class="hero-content">
            <hgroup class="hero-text-container">
                <h1>
                    Transforme dados em decisões.<br>
                    Transforme conversas em resultados.
                </h1>
                <p>Respostas rápidas, insights acionáveis e suporte 24/7. Tudo com a sua identidade.</p>
            </hgroup>
            <Button text="Experimente grátis por 7 dias" targetId="plans-section" class="free-trial"
                @buttonClick="$emit('navigateToSection', $event)" />
        </div>
    </section>
</template>

<script>
import Button from './Button.vue';
export default {
    name: 'Hero',
    components: {
        Button
    },
    emits: ['navigateToSection'],
    methods: {
        navigateToSection(sectionId) {
            const section = document.getElementById(sectionId);
            if (section) {
                section.scrollIntoView({ behavior: 'smooth' });
            }
        }
    }
};
</script>

<style>
.hero-wrapper {
    position: relative;
    width: 100%;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 0 1.5rem;
    overflow: hidden;
}

.hero-background {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: -1; 
}

.hero-content {
    position: relative;
    z-index: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    gap: 2rem;
    height: 100%;
    color: var(--text-primary-color);
    padding-top: 5rem; 
}

.hero-text-container {
    color: var(--text-secondary-color);
    max-width: 900px; 
}

.hero-text-container h1 {
    font-family: var(--font-family-serif);
    font-weight: var(--font-weight-bold);
    font-size: var(--font-size-title-hero);
    margin-bottom: 2rem;
}

.hero-text-container p {
    font-family: var(--font-family-sans-serif);
    font-size: clamp(1rem, 2vw, 1.2rem);
}

.free-trial {
    padding: 1.5rem 3rem;
    border: none;
    cursor: pointer;
    font-size: 1.1rem; 
    border-radius: 50px; 
    display: inline-flex;
    justify-content: center;
    align-items: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease; 
    margin-bottom: 4rem;
}

.free-trial:hover {
    transform: translateY(-3px); 
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2); 
}

@media (max-width: 768px) {
}
</style>