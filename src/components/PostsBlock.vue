<template>
    <section class="posts">
        <h2 class="posts-title">{{ posts.title }}</h2>
        <article
            v-for="(item, index) in posts.content"
            :key="index"
        >
          <h3>{{ item.title }}</h3>
          <div>{{ item.description }}</div>
          <p>{{ item.date }}</p>
          <router-link :to="item.link">подробнее</router-link>
        </article>
    </section>
</template>

<script>

export default {
    name: "PostsBlock",
    props: {
        posts: Object
    },
}
</script>
