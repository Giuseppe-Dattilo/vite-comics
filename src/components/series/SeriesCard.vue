<script>
export default {
    name: 'SeriesCard',
    props: {
        serie: Object
    }
}
</script>

<template>
    <div class="card">
        <img :src="serie.thumb" :alt="serie.series">
        <h3>{{ serie.series }}</h3>
    </div>
</template>

<style scoped lang="scss">
.card {
    padding: 10px;

    img {
        display: block;

        &:hover {
            transform: scale(1.1);
        }
    }

    h3 {
        margin-top: 5px;
        font-size: 15px;
        text-transform: uppercase;
        font-family: "Open Sans";
    }
}
</style>