<script>

export default {
    data() {
        return {
            contacts: [
                {
                    contactName: 'facebook',
                    img: 'src/assets/img/footer-facebook.png',
                },
                {
                    contactName: 'twitter',
                    img: 'src/assets/img/footer-twitter.png',
                },
                {
                    contactName: 'youtube',
                    img: 'src/assets/img/footer-youtube.png',
                },
                {
                    contactName: 'pinterest',
                    img: 'src/assets/img/footer-pinterest.png',
                },
                {
                    contactName: 'periscope',
                    img: 'src/assets/img/footer-periscope.png',
                },
            ]
        }
    }
}
</script>

<template>
<section class="credits container">
    <button>SIGN-UP NOW!</button>
    <div class="contact">
        <ul>
            <li><a href="#"><h3>FOLLOW US</h3></a></li>
            <li v-for="contact in contacts"><a href="#"><img :src="contact.img" :alt="contact.contactName"></a></li>
        </ul>
    </div>

</section>
</template>

<style lang="scss" scoped>
.credits {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.875rem 1.25rem;

    button {
        color: var(--lighter-color);
        padding: .9375rem;
        background-color: transparent;
        border: .0625rem solid var(--primary-color);
        cursor: pointer;
    }

    ul {
        display: flex;
        align-items: center;
        list-style: none;

        li:not(:last-child) {
            margin-right: 1.25rem;
        }

        a {
            text-decoration: none;
            color: var(--primary-color-dark);
        }
    }
}
</style>
