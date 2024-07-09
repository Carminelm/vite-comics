
<script>
export default {
    name: 'SingleComic',

    props: {
        thumb: String,
        price: String,
        series: String,
        type: String,
    }
}

</script>

<template>
    <article class="card">
        <a href="#">
            <div class="img-container">
                <img :src="thumb" :alt="series" :title="series + '\nPrice:' + price">
            </div>
            <span class="text-uppercase">{{ series }}</span>
        </a>
    </article>
</template>

<style lang="scss">
@use '../../styles/partials/variables' as *;



.card {
    width: calc(100%/6 - 2rem);
    margin: 1rem;

    a {
        color: $primary--color;
    }

    .img-container {
        margin-bottom: 1rem;
    }

    &:hover img {
        filter: contrast(1.5)
    }
}
</style>