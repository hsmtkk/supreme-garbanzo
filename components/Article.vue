<template>
    <v-card v-bind:title="props.title" v-bind:subtitle="props.subtitle" v-bind:text="props.text" />
</template>

<script setup lang="ts">
interface Props {
    title: string
    subtitle: string
    text: string
}

const props = defineProps<Props>()
</script>
