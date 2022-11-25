<script>
export default {
  data() {
    return {
        infos: [
            {
            img: 'src/assets/img/buy-comics-digital-comics.png',
            title: 'DIGITAL COMICS'
            },
            {
            img: 'src/assets/img/buy-comics-merchandise.png',
            title: 'DC MERCHAINDISE'
            },
            {
            img: 'src/assets/img/buy-comics-subscriptions.png',
            title: 'SUBSCRIPTION'
            },
            {
            img: 'src/assets/img/buy-comics-shop-locator.png',
            title: 'COMIC SHOP LOCATOR'
            },
            {
            img: 'src/assets/img/buy-dc-power-visa.svg',
            title: 'DC POWER VISA'
            },
        ]
    }
  }
}
</script>

<template>
    <section>
        <div class="container">
            <div class="cards" v-for="info in infos">
                <a href="#"><img :src="info.img" :alt="info.title"></a>
                <span>{{info.title}}</span>
            </div>
        </div>
    </section>    
</template>

<style lang="scss" scoped>
section {
    background-color: var(--primary-color);

    .container {
        display: flex;
        justify-content: space-around;
        padding: 2.8125rem;

        .cards {
            display: flex;
            align-items: center;
            max-height: 3.75rem;
            color: var(--lighter-color);

            a {
                width: 2.5rem;
                margin-right: .9375rem;

                img {
                    display: block;
                    width: 100%;
                }
            }

            span {
                cursor: pointer;
            }

        }
    }
}
</style>
