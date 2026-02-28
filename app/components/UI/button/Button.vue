<template>
  <button
      :class="classes"
      class="gap-2 max-w-max">
    <slot/>
    <NuxtImg v-if="props.icon"
             :src="iconSrc"
             class="max-w-6"/>
  </button>
</template>

<script lang="ts" setup>

interface Props {
  variant: 'primary' | 'inverse'
  iconSrc?: string
  direction?: 'left' | 'right' | 'none'
  icon: boolean
}

const props = withDefaults(defineProps<Props>(), {
  variant: "primary",
  iconSrc: 'https://cdn-icons-png.flaticon.com/512/535/535239.png',
  direction: 'none',
  icon: false,
})

const classes = computed(() => {
  const base = 'cursor-pointer rounded px-6 py-2 tracking-widest font-bold uppercase border-primary border-2 '

  const variants = {
    primary: 'bg-primary hover:bg-primary-foreground text-primary-foreground hover:text-foreground',
    inverse: 'bg-primary-foreground hover:bg-primary/10 text-foreground',
  }


  return [
    base,
    variants[props.variant],
  ].join(' ')
})

</script>

<style scoped>

</style>
