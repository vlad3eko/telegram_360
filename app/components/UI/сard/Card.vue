<template>
  <div class="p-5 rounded-2xl cursor-pointer max-w-max
              border hover:border-accent-foreground
              bg-card hover:bg-accent
              text-accent-foreground hover:text-foreground">
    <CardHeader
        v-if="props.cardHeaderImg
              || props.cardHeaderTitle
              || props.cardHeaderStatus"
        :card-header-img="props.cardHeaderImg"
        :card-header-title="props.cardHeaderTitle"
        :card-header-status="props.cardHeaderStatus"/>
    <CardTitle
        v-if="props.cardTitle"
        :card-title="props.cardTitle"/>
    <CardContent
        v-if="props.cardSubTitle
              || props.cardSubImage
              || props.cardSubDescription
              || cardTrigger"
        :card-sub-title="props.cardSubTitle"
        :card-sub-image="props.cardSubImage"
        :card-sub-description="props.cardSubDescription"
        :card-trigger="props.cardTrigger"/>
  </div>
</template>

<script lang="ts" setup>

import CardTitle from "~/components/UI/сard/CardTitle.vue";
import CardHeader from "~/components/UI/сard/CardHeader.vue";
import CardContent from "~/components/UI/сard/CardContent.vue";


export interface ICard {
  cardHeaderImg?: string
  cardHeaderTitle?: string
  cardHeaderStatus?: string
  cardTitle?: string
  cardSubTitle?: string
  cardSubDescription?: string
  cardSubImage?: string
  cardTrigger?: string
}

const props = defineProps<ICard>()
</script>

<style scoped>

</style>
