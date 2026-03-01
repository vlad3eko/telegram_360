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

import CardDescription from "~/components/UI/card/CardDescription.vue";
import CardTrigger from "~/components/UI/card/CardTrigger.vue";
import type {ICard} from "~/components/UI/card/Card.vue";

export type ICardContent = Pick<ICard, 'cardSubTitle' | 'cardSubImage'| 'cardSubDescription' | 'cardTrigger'>

const props = defineProps<ICardContent>()

</script>

<style scoped>

</style>
