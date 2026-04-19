<template>
    <router-link :to="{name: 'article', params:{id: article.id}}" class="card text-decoration-none">
        <img :src="article.image" class="card-img-top" alt="...">
        <div class="card-body">
            <h5 class="card-title">{{ article.title }}</h5>
            <p>{{ article.content }}</p>
        </div>
    </router-link>
</template>

<script>
export default {
    props: {
        article: Object
    }
}
</script>

<style scoped>
.card {
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);
}

.card h5 {
    color: rgb(75, 75, 75);
}

.card img {
    height: 200px;
}
</style>