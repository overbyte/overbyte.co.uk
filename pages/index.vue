<template>
    <div class="container">

        <nav>
            <div class="logo">
                Allandt Bik-Elliott
            </div>
            <a href="#home">Home</a>
            <a href="#work">Work</a>
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
        </nav>
        <div>
            <Logo />
            <h1>
                Hello!
            </h1>

            <h2>
                My name is Allandt (I'll tell you how it's pronounced, if you fancy a
                chat), a developer living in Hertford, a train-ride away from London.
            </h2>

            <h3>
                I have experience creating front-ends for websites, installations for
                events and mobile apps.
            </h3>

            <div class="links">
                <a href="https://nuxtjs.org/"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="button--green">
                    Documentation
                </a>
                <a href="https://github.com/nuxt/nuxt.js"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="button--grey">
                    GitHub
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {}
</script>

<style>
.container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.title {
    font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #35495e;
    letter-spacing: 1px;
}

.subtitle {
    font-weight: 300;
    font-size: 42px;
    color: #526488;
    word-spacing: 5px;
    padding-bottom: 15px;
}

.links {
    padding-top: 15px;
}
</style>
