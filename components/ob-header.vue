<template>
    <div class="main-nav">
        <a href="#home" class="logo">
            Allandt Bik-Elliott
        </a>

        <a href=""></a>
        <nav class="mobile-hidden">
            <a href="#home">Home</a>
            <a href="#work">Work</a>
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
        </nav>
    </div>
</template>

<style lang="scss">
.main-nav {
    display: flex;
    justify-content: space-between;
    padding: 1em;
    position: fixed;
    width: 100%;
    background-color: var(--matte);
    font-weight: 600;

    .logo {
        padding: 1em;
    }

    nav {
        a {
            display: inline-block;
            padding: 1em;
        }
    }
}
</style>
