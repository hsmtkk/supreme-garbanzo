<template>
    <BlogPage v-bind:id="id" />
</template>

<script setup lang="ts">
const route = useRoute()
const id = route.params.id
</script>