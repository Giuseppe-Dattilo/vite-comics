<script>

export default {
    nome: 'AppFooter',

}
</script>

<template>
    <footer>
        <!-- Footer top -->
        <nav class="footer-top">
            <div class="container">
                <div class="footer-row">
                    <div class="footer-col">
                        <ul>
                            <h4>DC COMICS</h4>
                            <li><a href="#">Characters</a></li>
                            <li><a href="#">Comics</a></li>
                            <li><a href="#">Movies</a></li>
                            <li><a href="#">TV</a></li>
                            <li><a href="#">Games</a></li>
                            <li><a href="#">Videos</a></li>
                            <li><a href="#">News</a></li>
                        </ul>
                        <h4>SHOP</h4>
                        <ul>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                        </ul>
                    </div>
                    <div class="footer-col">
                        <h4>DC</h4>
                        <ul>
                            <li><a href="#">Terms Of Use</a></li>
                            <li><a href="#">Privacy policy (New)</a></li>
                            <li><a href="#">Ad Choises</a></li>
                            <li><a href="#">Advertising</a></li>
                            <li><a href="#">Jobs</a></li>
                            <li><a href="#">Subscriptions</a></li>
                            <li><a href="#">Talent Workshops</a></li>
                            <li><a href="#">CPSC Certificates</a></li>
                            <li><a href="#">Ratings</a></li>
                            <li><a href="#">Shop Help</a></li>
                            <li><a href="#">Contact Us</a></li>
                        </ul>
                    </div>
                    <div class="footer-col">
                        <h4>SITES</h4>
                        <ul>
                            <li><a href="#">DC</a></li>
                            <li><a href="#">MAD Magazine</a></li>
                            <li><a href="#">DC Kids</a></li>
                            <li><a href="#">DC Universe</a></li>
                            <li><a href="#">DC Power Visa</a></li>
                        </ul>
                    </div>
                    <div>
                        <img src="../assets/img/dc-logo-bg.png" alt="logo-dc">
                    </div>
                </div>
            </div>
        </nav>

        <!-- Footer bottom -->
        <nav class="footer-bottom">
            <nav class="container">
                <div class="left-nav">
                    <button>SIGN UP NOW!</button>
                </div>
                <div class="right-nav">
                    <span>follow us</span>
                    <ul>
                        <li><a href="#"><img src="../assets/img/footer-facebook.png" alt="facebook"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-twitter.png" alt="twitter"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-youtube.png" alt="youtube"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-pinterest.png" alt="pinterest"></a></li>
                        <li><a href="#"><img src="../assets/img/footer-periscope.png" alt="periscope"></a></li>
                    </ul>
                </div>
            </nav>
        </nav>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    min-height: calc(100vh - 400px);

    .footer-top {
        min-height: calc(100% - 100px);
        background-image: url('../assets/img/footer-bg.jpg');
        background-size: cover;
        background-repeat: no-repeat;
        padding: 50px;
        position: relative;

        img {
            clip-path: inset(60px 0px 60px 0px);
            top: -111px;
            position: absolute;
        }

        .footer-row {
            display: flex;
        }

        .footer-col {
            flex-basis: 200px;

            h4 {
                text-transform: uppercase;
                margin-bottom: 10px;
                color: white;
                font-family: "Open Sans Condensed";
                font-size: 20px;
            }

            ul {
                list-style-type: none;
                margin-bottom: 10px;

                a {
                    color: grey;

                    &:hover {
                        color: white;
                    }
                }
            }
        }
    }

    .footer-bottom {
        height: 100px;
        background-color: #303030;

        nav {
            height: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;

            button {
                padding: 10px;
                background-color: transparent;
                border: 2px solid #0082f9;
                color: white;
                cursor: pointer;

                &:hover {
                    background-color: #0082f9;
                }
            }

            .right-nav {
                display: flex;
                justify-content: space-between;
                align-items: center;
                gap: 1.5rem;
            }

            span {
                font-size: 20px;
                color: #0082f9;
                text-transform: uppercase;
                font-family: "Open Sans Condensed";
            }

            ul {
                display: flex;
                gap: 20px;
                list-style-type: none;

                a:hover {
                    filter: brightness(150%)
                }
            }
        }
    }

}
</style>