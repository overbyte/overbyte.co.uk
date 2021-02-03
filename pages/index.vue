<template>
    <div>
        <section id="home" class="hero">
            <div>
                <h1 class="hello">{{ home.title }}</h1>
                <h2>{{ home.subtitle }}</h2>
                <h3>{{ home.body }}</h3>

            </div>
        </section>

        <section id="work">
            <ObJob v-for="job in jobs" :job="job"></ObJob>
        </section>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    asyncData(context) {
        return axios
            .get(`https://api.storyblok.com/v1/cdn/spaces/me/?token=${process.env.SB_TOKEN}`)
            .then(res => axios.get(`https://api.storyblok.com/v1/cdn/stories/?version=published&token=${process.env.SB_TOKEN}&cv=${res.data.space.version}`))
            .then(res => {
                return {
                    jobs: res.data.stories
                        .filter(item => item.name === 'work')[0]
                        .content.jobs,
                    home: res.data.stories
                        .filter(item => item.name ==='home')[0]
                        .content,
                };
            })
        ;
    },
}
</script>

<style lang="scss">
.hero {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 3em;
    background-color: lightblue;

    h1 {
        font-size: 6em;
        font-weight: 300;
        color: var(--secondary);
    }
}
#work {
    color: var(--tertiary);
}
</style>
