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
    max-width: 500px;
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
    color: var(--secondary-color);
    transform: translateY(-5px);
}

.project-image {
    height: 400px;
    width: 100%;
    object-fit: cover; 
}

.project-info {
    padding: 1rem;
}

</style>