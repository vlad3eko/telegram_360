<template>
  <section :class="classes">
      <slot/>
  </section>
</template>

<script lang="ts" setup>

interface Props {
  directionRow?: boolean
}

const props = defineProps<Props>()

const classes = computed(() => {
  const base = 'w-full bg-inherit block py-30 min-h-[80vh]'


  return [
    base,
    props.directionRow ?
        'flex justify-center items-center'
        :
        'px-10'
  ].join(' ')
})

</script>

<style scoped>

</style>
