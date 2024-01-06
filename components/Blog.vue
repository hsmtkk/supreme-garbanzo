<template>
    <v-container>
        <Article v-for="article in data" v-bind:key="article.id" v-bind:title="article.title" v-bind:subtitle="article.date"
            v-bind:text="article.description" />
    </v-container>
</template>

<script setup lang="ts">
const { data } = await useAsyncData("blogQuery", () => {
    return queryContent("/blog").find()
})
</script>
