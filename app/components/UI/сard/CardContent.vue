<template>
  <div class="flex items-center justify-between">
    <CardDescription
        v-if="props.cardSubTitle
              || props.cardSubImage
              || props.cardSubDescription"
        :card-sub-title="props.cardSubTitle" :card-sub-image="props.cardSubImage" :card-sub-description="props.cardSubDescription"/>
    <CardTrigger
        v-if="props.cardTrigger"
        :card-trigger="props.cardTrigger"/>
  </div>
</template>

<script lang="ts" setup>

import CardDescription from "~/components/UI/сard/CardDescription.vue";
import CardTrigger from "~/components/UI/сard/CardTrigger.vue";
import type {ICard} from "~/components/UI/сard/Card.vue";

export type ICardContent = Pick<ICard, 'cardSubTitle' | 'cardSubImage'| 'cardSubDescription' | 'cardTrigger'>

const props = defineProps<ICardContent>()

</script>

<style scoped>

</style>
