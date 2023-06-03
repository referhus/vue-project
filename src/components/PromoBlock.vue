<template>
    <section class="promo">
        <h1 class="promo-title">
            {{ promo.title }}
        </h1>
        <div class="promo-desc">
            {{ promo.description }}
        </div>
    </section>
</template>

<script>
export default {
    name: 'PromoBlock',
    props: {
        promo: Object
    }
}
</script>

<style scoped>
</style>
