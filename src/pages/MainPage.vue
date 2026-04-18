<template>
    <div class="row py-3">
        <div class="col">
            <h1>Новости</h1>
        </div>
        <div class="row">
            <div class="col-lg-3 col-md-4 col-sm-6 col-12 mb-2" v-for="article in articles" :key="article.id">
                <a href="#" class="card text-decoration-none">
                    <img :src="article.img" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">{{ article.title }}</h5>
                    </div>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
 data() {
    return {
        articles: [
            {
                id: 1,
                title: 'Новость дня',
                img: 'https://www.sostav.ru/images/news/2019/04/01/9iithyjt_md.jpg'
            },
            {
                id: 2,
                title: 'Новость ',
                img: 'https://www.sostav.ru/images/news/2019/04/01/9iithyjt_md.jpg'
            }
        ]
    }
 }
}
</script>

<style>
.card img {
    height: 200px;
}
</style>