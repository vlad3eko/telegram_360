<template>
  <button
      :class="[
          classes,
          props.direction === 'right' ? '' : 'flex-row-reverse',
          `flex gap-2 max-w-max`]">
    <slot/>
    <NuxtImg v-if="props.icon"
             :src="iconSrc"
             class="max-w-6"/>
  </button>
</template>

<script lang="ts" setup>

interface Props {
  variant?: 'primary' | 'inverse' | 'disable'
  iconSrc?: string
  direction?: 'right' | 'inverse'
  isDisable?: boolean
  icon?: boolean
}

const props = withDefaults(defineProps<Props>(), {
  variant: 'primary',
  iconSrc: 'https://cdn-icons-png.flaticon.com/512/535/535239.png',
  direction: 'right',
  isDisable: false,
  icon: false,
})



const classes = computed(() => {
  const base = ' rounded-2xl px-6 py-2 tracking-widest font-bold uppercase'

  const variants = {
    primary: 'bg-primary hover:bg-primary-foreground text-primary-foreground hover:text-foreground cursor-pointer',
    inverse: 'bg-accent/50 hover:bg-primary text-foreground hover:text-primary-foreground cursor-pointer',
    disable: 'bg-primary text-primary-foreground/80 cursor-not-allowed'
  }


  return [
    base,
    variants[props.variant],
  ].join(' ')
})

</script>

<style scoped>

</style>
