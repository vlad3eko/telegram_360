<template>
  <div class="relative overflow-hidden rounded-2xl">
    <NuxtImg v-if="props.cardHeaderImg" :src="props.cardHeaderImg" class="rounded-2xl max-w-75 min-w-75 max-h-75 min-h-75 object-cover opacity-90"/>
    <span v-if="cardHeaderTitle" class="absolute top-3 right-3 bg-background/60 text-accent-foreground p-2 m-2 rounded">{{cardHeaderTitle}}</span>
    <span v-if="cardHeaderStatus" class="absolute bottom-3 left-3 bg-price  text-primary-foreground p-2 m-2 rounded">{{cardHeaderStatus}}</span>
  </div>
</template>

<script lang="ts" setup>

import type {ICard} from "~/components/UI/card/Card.vue";

export type ICardHeader = Pick<ICard, 'cardHeaderImg' | 'cardHeaderTitle' | 'cardHeaderStatus'>

const props = defineProps<ICardHeader>()

</script>

<style scoped>

</style>
