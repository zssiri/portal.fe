<template>
    <div class="row py-3">
        <div class="col">
            <h1>Новости</h1>
        </div>
        <div class="row">
            <div class="col-lg-3 col-md-4 col-sm-6 col-12 mb-2" v-for="article in articles" :key="article.id">
                <ArticleCard :article="article"/>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
import ArticleCard from '@/components/ArticleCard.vue';

export default {
    components: {
        ArticleCard
    },
    data() {
        return {
            articles: [
                
            ]
        }
    },
    methods: {
        async LoadArticles() {
            const response = await axios.get("http://portal.be/api/articles");
            this.articles = response.data;
        }
    },
    mounted() {
        this.LoadArticles();
    }
}
</script>

<style>
body {
    background-color: rgb(240, 240, 240);
}

h1 {
    color: rgb(75, 75, 75);
    text-align: center;
}

</style>