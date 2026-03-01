<template>
  <div class="my-3 font-bold text-xl">
    {{ props.cardTitle }}
  </div>
</template>

<script lang="ts" setup>

import type {ICard} from "~/components/UI/card/Card.vue";

export type ICardTitle = Pick<ICard, 'cardTitle'>

const props = defineProps<ICardTitle>()

</script>

<style scoped>

</style>
