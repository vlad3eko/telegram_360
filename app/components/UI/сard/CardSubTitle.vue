<template>
  <div class="text-muted-foreground opacity-80">
    {{ props.cardSubTitle }}
  </div>
</template>

<script lang="ts" setup>

import type {ICardDescription} from "~/components/UI/сard/CardDescription.vue";

export type ICardSubTitle = Pick<ICardDescription, 'cardSubTitle'>

const props = withDefaults(defineProps<ICardSubTitle>(), {
  cardSubTitle: ''
})

</script>

<style scoped>

</style>
