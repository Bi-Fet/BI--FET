<template>
    <div class="navbar-wrapper">
        <div class="navbar-wrap">
            <img src="../assets/images/logo-bifet.svg" alt="Logo da Bi-Fet" class="logo">
            <nav>
                <ul>
                    <li>
                        <RouterLink to="/about">Sobre</RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/product">Produto</RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/plans">Planos</RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/contact">Contato</RouterLink>
                    </li>
                </ul>
            </nav>
            <button class="demo">Agendar demonstração</button>
        </div>
    </div>
</template>

<style scoped>
.navbar-wrapper {
    position: absolute;
    top: 10px;
    left: 0;
    width: 100%;
    z-index: 10;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 5rem;
}

.navbar-wrap {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
}

.navbar-wrap nav {
    background-color: var(--tertiary-color);
    padding: 0.5rem 4rem;
    border-radius: 3.125rem;
}

.navbar-wrap nav ul {
    display: flex;
    list-style: none;
    gap: 64px;
}

.navbar-wrap nav li a {
    font-size: 1.125rem;
    color: var(--text-secondary-color);
    text-decoration: none;
}
</style>