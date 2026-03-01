<template>
  <div>
    <CardSubTitle
        v-if="props.cardSubTitle"
        :card-sub-title="props.cardSubTitle"/>
    <CardSubDescription
        v-if="props.cardSubImage
              || props.cardSubDescription"
        :card-sub-image="props.cardSubImage" :card-sub-description="props.cardSubDescription"/>
  </div>
</template>

<script lang="ts" setup>
import CardSubDescription from "~/components/UI/card/CardSubDescription.vue";
import CardSubTitle from "~/components/UI/card/CardSubTitle.vue";
import type {ICard} from "~/components/UI/card/Card.vue";

export type ICardDescription = Pick<ICard, 'cardSubTitle' | 'cardSubImage' | 'cardSubDescription'>

const props = defineProps<ICardDescription>()

</script>

<style scoped>

</style>
