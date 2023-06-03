<template>
    <div class="home">
        <PromoBlock v-if="promo" :promo="promo"/>
        <PostsBlock v-if="posts" :posts="posts"/>
    </div>
</template>

<script>
// @ is an alias to /src
import axios from "axios";

import PromoBlock from '@/components/PromoBlock.vue'
import PostsBlock from '@/components/PostsBlock.vue'

export default {
    name: 'HomeView',
    components: {
        PromoBlock,
        PostsBlock
    },
    data() {
        return {
            promo: null,
            posts: null,
        }
    },
    created() {
        axios
            .get('/api/data.json')
            .then(response => {
                this.promo = response.data.promo
                this.posts = response.data.posts
            })
    }

}
</script>
