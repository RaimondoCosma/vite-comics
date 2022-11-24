<script>
export default {
  data() {
    return {
        navList: ['CHARACTERS', 'COMICS', 'MOVIES', 'TV', 'GAMES', 'COLLECTIBLES', 'VIDEOS', 'FANS', 'NEWS', 'SHOP'],
        navIndex: 0,
    }
  },
  methods: {
    getIndex(index){
        this.navIndex = index;
    }
  }
}
</script>

<template>
<nav>
    <ul>
        <li v-for="link, index in navList" @click="getIndex(index)" :class="{active: index === navIndex}">{{link}}</li>
    </ul>
</nav>
</template>

<style lang="scss" scoped>
    .active {
        position: relative;
        color: var(--primary-color-dark);

        &::after {
            position: absolute;
            content: '';
            height: .3125rem;
            bottom: 0;
            left: 0;
            width: 100%;
            background-color: var(--primary-color-dark);
        }
    }
    ul {
        display: flex;
        list-style: none;

        li {
            cursor: pointer;
            padding: 3.125rem 0;
            transition: all 0.3s ease-out;
        
            &:not(:last-child) {
            margin-right: 1.875rem;
            }
        }

    }
</style>