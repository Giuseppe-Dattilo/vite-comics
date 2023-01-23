<script>
import Jumbo from './Jumbo.vue'
export default {
    nome: 'Appheader',
    components: { Jumbo },
    data() {
        return {
            links: [
                {
                    text: 'Characters',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    url: '#',
                    current: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    url: '#',
                    current: false,
                },
                {
                    text: 'News',
                    url: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    url: '#',
                    current: false,
                },
            ]
        }
    }
};
</script>

<template>
    <header class="container">
        <nav>
            <figure>
                <a href="#"><img src="../assets/img/dc-logo.png" alt="DC"></a>
            </figure>
            <ul>
                <li v-for="link in links" :key="link.text">
                    <a :href="link.url" v-text="link.text" :class="{ 'active': link.current }"></a>
                </li>
            </ul>
        </nav>
    </header>
    <jumbo></jumbo>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins' as *;

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 0;
    font-family: "Open Sans Condensed";
    height: 100px;

    img {
        height: 80px;
    }
}

ul {
    @include center_flex;
    margin: 30px;
    padding: 0;

    li {
        list-style-type: none;

        a {
            padding: 10px;
            color: black;
            text-transform: uppercase;

            &.active {
                color: blue;
            }

            &:hover {
                background-color: lightblue;
            }

        }
    }
}
</style>