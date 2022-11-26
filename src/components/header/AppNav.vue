<script>
export default {
  data() {
    return {
      navList: [
        "CHARACTERS",
        "COMICS",
        "MOVIES",
        "TV",
        "GAMES",
        "COLLECTIBLES",
        "VIDEOS",
        "FANS",
        "NEWS",
        "SHOP",
      ],
      navIndex: 0,
      hamburgerAnimation: false,
    };
  },
  methods: {
    getIndex(index) {
      this.navIndex = index;
    },
    animateBurger() {
      this.hamburgerAnimation = !this.hamburgerAnimation;
    },
  },
};
</script>

<template>
  <nav>
    <div class="hamburger" @click="animateBurger">
      <div
        class="hamburger-menu"
        :class="{ 'ham-animation': hamburgerAnimation }"
      ></div>
    </div>
    <ul :class="{ 'show-ul': hamburgerAnimation }">
      <li
        v-for="(link, index) in navList"
        @click="getIndex(index)"
        :class="{ active: index === navIndex }"
      >
        {{ link }}
      </li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
nav {
  display: flex;
  align-items: center;

  @media screen and (max-width: 768px) {
    padding: calc(1.5625rem - 0.1094rem) 0;
  }
}

.hamburger {
  cursor: pointer;
  height: 30px;
  display: flex;
  align-items: center;
}
.hamburger-menu {
  position: relative;
  width: 1.875rem;
  height: 0.3125rem;
  background-color: var(--darkest-color);
  border-radius: 0.3125rem;
  z-index: 100;
  display: none;
  transition: 0.2s background-color linear 0.2s;

  &::before,
  &::after {
    content: "";
    position: absolute;
    height: 0.3125rem;
    background-color: #000;
    border-radius: 0.3125rem;
    transition: 0.4s transform, width linear;
  }
  &::after {
    top: 0.625rem;
    left: 0;
    width: 1.5625rem;
  }
  &::before {
    top: -0.625rem;
    left: 0;
    width: 1.25rem;
  }

  @media screen and (max-width: 768px) {
    display: block;
  }
}
.ham-animation {
  background-color: transparent;

  &::after {
    top: 0;
    width: 1.875rem;
    transform: rotate(225deg);
  }
  &::before {
    top: 0;
    width: 1.875rem;
    transform: rotate(-225deg);
  }
}
.active {
  position: relative;
  color: var(--primary-color-dark);

  &::after {
    position: absolute;
    content: "";
    height: 0.3125rem;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: var(--primary-color-dark);
  }
}
ul {
  display: flex;
  align-items: center;
  list-style: none;
  z-index: 100;
  transition: right 0.4s ease-out;

  li {
    cursor: pointer;
    padding: 3.125rem 0;
    transition: all 0.3s ease-out;

    &:not(:last-child) {
      margin-right: 1.875rem;

      @media screen and (max-width: 992px) {
        margin-right: 0.9375rem;
      }
    }
    @media screen and (max-width: 992px) {
      padding: 1.875rem 0;
      font-size: 0.875rem;
    }
    @media screen and (max-width: 768px) {
      background-color: var(--lighter-color);
      width: 100%;
      padding: 1.25rem 0;
      border: 1px solid var(--darkest-color-light);
      margin-right: 0.9375rem;
      text-align: center;

      &:hover {
        background-color: var(--secondary-color);
      }
    }
  }
  @media screen and (max-width: 768px) {
    flex-direction: column;
    position: fixed;
    top: 73px;
    right: -230px;
    height: 100vh;
    width: 200px;
    box-shadow: -20px 7px 10px 0px #000000;
  }
}
.show-ul {
  right: -10px;
}
</style>
