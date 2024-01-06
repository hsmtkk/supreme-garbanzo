<template>
    <BlogListItem v-for="article in data" v-bind:key="article.id" v-bind:article="article" />
</template>

<script setup lang="ts">
const { data } = await useAsyncData("blogQuery", () => {
    return queryContent("/blog").sort({ id: -1 }).find()
})
</script>
