<script>
export default {
  data() {
    return {
      contacts: [
        {
          contactName: "facebook",
          img: "src/assets/img/footer-facebook.png",
        },
        {
          contactName: "twitter",
          img: "src/assets/img/footer-twitter.png",
        },
        {
          contactName: "youtube",
          img: "src/assets/img/footer-youtube.png",
        },
        {
          contactName: "pinterest",
          img: "src/assets/img/footer-pinterest.png",
        },
        {
          contactName: "periscope",
          img: "src/assets/img/footer-periscope.png",
        },
      ],
    };
  },
};
</script>

<template>
  <section class="credits container">
    <button>SIGN-UP NOW!</button>
    <div class="contact">
      <ul>
        <li>
          <a href="#"><h3>FOLLOW US</h3></a>
        </li>
        <li v-for="contact in contacts">
          <a class="icons" href="#"
            ><img :src="contact.img" :alt="contact.contactName"
          /></a>
        </li>
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
    padding: 0.9375rem;
    background-color: transparent;
    border: 0.0625rem solid var(--primary-color);
    cursor: pointer;
    transition: background-color 0.3s linear;
    &:hover {
      background-color: var(--secondary-color);
    }
    @media screen and (max-width: 576px) {
      padding: 0.625rem;
    }
  }

  ul {
    display: flex;
    align-items: center;
    list-style: none;

    li:not(:last-child) {
      margin-right: 1.25rem;
      @media screen and (max-width: 576px) {
        margin-right: 0.625rem;
      }
    }

    a {
      text-decoration: none;
      color: var(--primary-color-dark);
    }
  }
  @media screen and (max-width: 576px) {
    li h3 {
      font-size: 1rem;
    }
    .icons img {
      width: 1.5625rem;
      height: 1.5625rem;
    }
  }
}
</style>
