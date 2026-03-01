<template>
    <Button v-if="props.cardTrigger">
      {{ props.cardTrigger }}
    </Button>
</template>

<script lang="ts" setup>
import Button from "~/components/UI/button/Button.vue";
import type {ICardContent} from "~/components/UI/card/CardContent.vue";

type ICardTrigger = Pick<ICardContent, 'cardTrigger'>

const props = defineProps<ICardTrigger>()
</script>

<style scoped>

</style>
