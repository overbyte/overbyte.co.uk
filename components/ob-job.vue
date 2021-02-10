<template>
    <div class="job">
        <h2>{{ job.content.title }}</h2>
        <h3>{{ job.content.type }}</h3>
        <h4>{{ job.content.agency }} 
            | {{ job.content.client }} 
            | {{ job.content.year }}
        </h4>
        <p>{{ job.content.body }}</p>
        <ul>
            <li v-for="tag in job.tag_list">{{ tag }}</li>
        </ul>
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
        color: var(--secondary);
    }

    p {
        color: var(--primary);
    }

    ul {
        margin-top: 1em;
        padding: 0;

        li {
            font-size: 0.9em;
            display: inline-block;
            margin: 0 0.5rem 0.5rem 0;
            padding: 0.5rem;
            background-color: var(--tag-bg);
            color: var(--tag-col);
            border-radius: 1rem;
        }
    }
}
</style>
