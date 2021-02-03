<template>
    <div class="job">
        <h2>{{ job.title }}</h2>
        <h3>{{ job.type }}</h3>
        <h4>{{ job.agency }} :: {{ job.client }}</h4>
        <p>{{ job.body }}</p>
    </div>
</template>

<script>
export default {
    props: {
        job: Object,
    },
}
</script>

<style lang="scss">
.job {
    padding: 2rem;
    border-bottom: 1px solid var(--primary);
    background-color: var(--background);

    h2 {
        margin-top: 0;
    }

    h3 {
        font-weight: 700;
        font-size: 3em;
        color: rgba(255, 255, 255, 0.3);
        margin-top: -0.75em;
        margin-left: 1em;
    }

    h4 {
        font-weight: 400;
    }

    p {
        color: var(--primary);
    }
}
</style>
