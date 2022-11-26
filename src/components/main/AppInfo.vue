<script>
export default {
  data() {
    return {
      infos: [
        {
          img: "src/assets/img/buy-comics-digital-comics.png",
          title: "DIGITAL COMICS",
        },
        {
          img: "src/assets/img/buy-comics-merchandise.png",
          title: "DC MERCHAINDISE",
        },
        {
          img: "src/assets/img/buy-comics-subscriptions.png",
          title: "SUBSCRIPTION",
        },
        {
          img: "src/assets/img/buy-comics-shop-locator.png",
          title: "COMIC SHOP LOCATOR",
        },
        {
          img: "src/assets/img/buy-dc-power-visa.svg",
          title: "DC POWER VISA",
        },
      ],
    };
  },
};
</script>

<template>
  <section>
    <div class="container">
      <div class="cards" v-for="info in infos">
        <a href="#"><img :src="info.img" :alt="info.title" /></a>
        <span>{{ info.title }}</span>
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
    @media screen and (max-width: 768px) {
      overflow-x: auto;
      justify-content: flex-start;
      padding: 2.8125rem 0;
    }

    .cards {
      display: flex;
      align-items: center;
      color: var(--lighter-color);
      @media screen and (max-width: 768px) {
        width: 9.375rem;
        flex-shrink: 0;
      }

      a {
        display: flex;
        align-items: center;
        justify-content: flex-end;
        width: 3.75rem;
        height: 3.75rem;
        margin-right: 0.625rem;

        @media screen and (max-width: 992px) {
          width: 2.5rem;
          height: 2.5rem;
        }

        img {
          display: block;
          max-height: 100%;
          max-width: 100%;
        }
      }

      span {
        cursor: pointer;
        @media screen and (max-width: 992px) {
          font-size: 0.875rem;
        }
        &:hover {
          text-decoration: underline;
        }
      }
    }
  }
}
</style>
