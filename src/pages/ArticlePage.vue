<template>
    <h2>{{ article.title }}</h2>
    <div class="container">
        <img :src="article.image" class="card-img-top" alt="...">
    </div>
    <p>{{ article.content }}</p>
</template>

<script>
import axios from 'axios';

export default {
    data() {
        return {
            articleId: this.$route.params.id,
            article: {}
        }
    },
    watch: {
        "$route.params.id": function (newId) {
            this.articleId = newId;
            this.loadArticle();
        }
    },
    methods: {
        async loadArticle() {
            const respons = await axios.get("http://portal.be/api/articles/" + this.articleId)
            this.article = respons.data
        }
    },
    mounted() {
        this.loadArticle();
    }
}
</script>

<style scoped>
.container {
    display: flex;
    justify-content: center;
}

img {
    height: 200px;
    max-width: 500px;
}
</style>