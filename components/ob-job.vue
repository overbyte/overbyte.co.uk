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

    h4 {
        font-weight: 300;
    }

    p {
        color: var(--primary);
    }
}
</style>
