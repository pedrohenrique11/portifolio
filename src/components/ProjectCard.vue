<script>
    export default {
        props: {
            link: String,
            title: String,
            text: String,
            img: String
        }
    }
</script>

<template>
    <a :href="link" class="project-link">
        <div class="project-container">
            <img :src="img" :alt="title" class="project-image">
            <div class="project-info">
                <h4>{{ title }}</h4>
                <p>{{ text }}</p>
            </div>
        </div>
    </a>
</template>

<style scoped>
.project-link {
    padding: 0;
    text-decoration: none;
}

.project-container {
    display: flex;
    flex-direction: column;

    padding: 0;
    margin-bottom: 1rem;

    color: #fff;
    background-color: #2D2E32;

    border-radius: 8px;
    overflow: hidden;
    transition: transform 0.3s ease;
}

.project-container:hover {
    color: hsla(160, 100%, 37%, 1);;
    transform: translateY(-5px);
}

.project-image {
    height: auto;
}

.project-info {

    padding: 1rem;
}

@media (min-width: 768px) {
    .project-container {
        flex-direction: row;
    }

    .project-image {
        width: auto;
        max-width: 300px; 
        height: 200px;
    }
}
</style>