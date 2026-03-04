<template>
    <span >{{ tweened.number.toFixed(0) }}{{count.letter}}</span>
</template>

<script lang="ts" setup>
import gsap from 'gsap'

interface ICount{
  count?: number | string
  letter?: string
}

const count = defineProps<ICount>()

const number = ref<number>(0)

const tweened = reactive({
  number: Math.floor(Math.random() * 20000)
})

const resetNumber = () => {
  return number.value = Number(toRaw(count).count)
}

watch(number, (n) => {
  gsap.to(tweened, { duration: 1.5, number: Number(n) || 0 })
})

onMounted((event: ICount) => {
  resetNumber()
})
</script>

<style scoped>

</style>
