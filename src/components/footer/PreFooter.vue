<script>
export default {
  data() {
    return {
        dcComics: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News'],
        shop: ['Shop DC', 'Shop DC Collectibles'],
        dc: ['Terms of Use', 'Privacy policy (New)', 'Ad Choise', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Rating', 'Shop Help', 'Contact Us'],
        sites: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],
    }
  }
}
</script>

<template>
    <section class="jumbotron">
        <div class="links-utility container">

            <div>
                <div>
                    <h3>DC COMICS</h3>
                    <ul>
                        <li v-for="comic in dcComics"><a href="#">{{comic}}</a></li>
                    </ul>
                </div>
                <div>
                    <h3>SHOP</h3>
                    <ul>
                        <li v-for="item in shop"><a href="#">{{item}}</a></li>
                    </ul>
                </div>
            </div>
            <div>
                <h3>DC</h3>
                <ul>
                    <li v-for="link in dc"><a href="#">{{link}}</a></li>
                </ul>
            </div>
            <div>
                <h3>SITES</h3>
                <ul>
                    <li v-for="site in sites"><a href="#">{{site}}</a></li>
                </ul>
            </div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
    .jumbotron {
        background-image: url('../../assets/img/footer-bg.jpg');
        background-size: cover;

        .links-utility {
            background-image: url('../../assets/logo/dc-logo-bg.png');
            background-repeat: no-repeat;
            background-position: right center;
            display: flex;

            ul {
                list-style: none;
                margin: 0 1.25rem 1.25rem 0;

                li {
                    padding: .3125rem;
                }

                a {
                    text-decoration: none;
                    color: var(--secondary-color);
                }
            }

            h3 {
                color: var(--lighter-color);
                margin-bottom: 1.25rem;
                margin-top: 3.125rem;
                padding: .3125rem;
            }
        }
    }
</style>
