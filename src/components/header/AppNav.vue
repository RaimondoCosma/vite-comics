<script>
export default {
  data() {
    return {
        navList: ['CHARACTERS', 'COMICS', 'MOVIES', 'TV', 'GAMES', 'COLLECTIBLES', 'VIDEOS', 'FANS', 'NEWS', 'SHOP']
    }
  }
}
</script>

<template>
<nav>
    <ul>
        <li v-for="link in navList">{{link}}</li>
    </ul>
</nav>
</template>

<style lang="scss" scoped>
    ul {
        display: flex;
        list-style: none;

        li {
            cursor: pointer;
            padding: 3.125rem 0;
        
            &:not(:last-child) {
            margin-right: 1.875rem;
            }
        }

    }
</style>