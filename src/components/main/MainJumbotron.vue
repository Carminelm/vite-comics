<script>

import SingleComic from './SingleComic.vue';
console.log(json)
import json from './../../assets/json/dc-comics.json';;

export default {
    name: 'MainJumbotron',

    components: {
        SingleComic,
    },

    data() {
        return {
            json,
        }
    },
}
</script>

<template>
    <section id="jumbotron">
        <div class="background"></div>

        <section id="comics-container" class="container p-relative">
            <h2 class="title text-uppercase p-absolute">Current Series</h2>

            <div class="comics-container d-flex wrap">
                <SingleComic v-for="comicInfo in json" :thumb="comicInfo.thumb" :price="comicInfo.price"
                    :series="comicInfo.series" :type="json.type" />
            </div>

            <div class="btn-container d-flex justify-center">
                <a href="#" class="btn text-uppercase">Load More</a>
            </div>
        </section>
    </section>
</template>

<style scoped lang="scss">
@use '../../styles/partials/variables' as *;




.background {
    background-image: url('../../assets/img/jumbotron.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    height: 350px;
}

#comics-container {
    background-color: $secondary--color;
    font-size: 0.7rem;

    .btn,
    .title {
        background-color: $complementary--color;
        display: inline-block;
        padding: 0.7rem 0;

        &.title {
            padding-left: 2rem;
            padding-right: 2rem;
        }
    }

    .title.p-absolute {
        bottom: calc(100% - 1.2rem);
    }

    a.btn {
        padding-left: 3rem;
        padding-right: 3rem;
        color: $primary--color;
        font-weight: bold;
        margin-top: 1rem;
    }
}
</style>