<template>
    <div>
        <h3>{{ props.article.title }}</h3>
        <p>{{ props.article.excerpt }}</p>
        <p>{{ props.article.date }}</p>
        <NuxtLink v-bind:to="{ name: `blog-id`, params: { id: props.article.id } }">Read More</NuxtLink>
    </div>
    <div>
        <NuxtImg v-bind:src="props.article.image" fit="cover" />
    </div>
</template>

<script setup lang="ts">
import type { Article } from "@/interfaces"

interface Props {
    article: Article
}

const props = defineProps<Props>()
</script>
