<template>
  <button :class="classes">
    <slot/>
  </button>
</template>

<script lang="ts" setup>

interface Props {
  variant: 'primary' | 'inverse'
}

const props = withDefaults(defineProps<Props>(), {
  variant: "primary"
})

const classes = computed(() => {
  const base = 'cursor-pointer rounded px-6 py-2 tracking-widest font-bold'

  const variants = {
    primary: 'bg-primary hover:bg-primary-foreground text-primary-foreground hover:text-foreground border-primary border-2 uppercase',
    inverse: 'text-foreground border-primary border-2 uppercase'
  }

  return [
      base,
      variants[props.variant],
  ].join(' ')
})

</script>

<style scoped>

</style>
