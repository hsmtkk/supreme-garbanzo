<template>
    <NuxtImg v-bind:src="data.image" fit="cover" />
    <h1>{{ data.title }}</h1>
    <p>{{ data.date }}</p>
    <p>{{ data.description }}</p>
</template>

<script setup lang="ts">
interface Props {
    id: string
}

const props = defineProps<Props>()

const { data } = await useAsyncData("blogQuery", () => {
    return queryContent("/blog").where({ id: props.id }).findOne()
})
</script>
