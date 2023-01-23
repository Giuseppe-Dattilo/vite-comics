<script>
import SeriesCard from './series/SeriesCard.vue';
export default {
    nome: 'AppMain',
    components: { SeriesCard },
    props: {
        series: Array
    },
    data() {
        return {
            elements: [
                {
                    text: 'digital comics',
                    pic: 'buy-comics-digital-comics.png',
                    url: '#'
                },
                {
                    text: 'Dc merchandise',
                    pic: 'buy-comics-merchandise.png',
                    url: '#'
                },
                {
                    text: 'subscriptions',
                    pic: 'buy-comics-subscriptions.png',
                    url: '#'
                },
                {
                    text: 'comic shop locator',
                    pic: 'buy-comics-shop-locator.png',
                    url: '#'
                },
                {
                    text: 'digital comics',
                    pic: 'buy-dc-power-visa.svg',
                    url: '#'
                },
            ]
        }
    },
    methods: {
        buildImagePath(pic) {
            return new URL(`../assets/img/${pic}`, import.meta.url).href;
        },
    }
}


</script>

<template>
    <main>
        <section id="comics">
            <div class="container">
                <h2>CURRENT SERIES</h2>
                <div class="container card-container">
                    <series-card v-for="serie in series" :key="serie.thumb" :serie="serie"></series-card>
                </div>
            </div>
        </section>
        <section id="dc">
            <div class="container">
                <div class="row">
                    <ul>
                        <li v-for="element in elements" :key="element.text">
                            <a :href="element.url"><img :src="buildImagePath(element.pic)" :alt="element.text">
                                <span>{{ element.text }}</span>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
#comics {
    background-color: black;
    color: white;
    padding: 4rem 1rem;
    min-height: 150px;

    .card-container {
        display: flex;
        flex-wrap: wrap;
        margin-top: 2rem;

        .card {
            flex-basis: calc(100%/6);
        }
    }
}

#dc {
    background-color: #0082f9;
    color: white;
    padding: 3rem 1rem;
    height: 150px;

    .row {
        display: flex;
        align-items: center;
        justify-content: space-around;
        font-size: 13px;
    }

    ul {
        display: flex;
        gap: 70px;

        li {
            list-style-type: none;

            a {
                display: flex;
                align-items: center;

                &:hover {
                    transform: scale(1.2);
                }
            }
        }

        span {
            color: white;
            text-transform: uppercase;
        }

        img {
            height: 50px;
            margin-right: 10px;
        }
    }
}
</style>