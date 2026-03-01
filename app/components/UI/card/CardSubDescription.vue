<template>
  <div class="font-bold flex">
    <NuxtImg
        v-if="props.cardSubImage"
        :src="props.cardSubImage" class="max-w-5"/>
    {{ props.cardSubDescription }}
  </div>
</template>

<script lang="ts" setup>

import type {ICardDescription} from "~/components/UI/card/CardDescription.vue";

export type ICardSubDescription = Pick<ICardDescription, 'cardSubDescription' | 'cardSubImage'>

const props = defineProps<ICardSubDescription>()
</script>

<style scoped>

</style>
