<template>
  <div :class="classes">
    <NuxtImg src="/logo.png"/>
  </div>
</template>

<script lang="ts" setup>

interface ILogo {
  variant?: 'sm' | 'md' | 'lg' | 'fullWidth'
}

const props = withDefaults(defineProps<ILogo>(), {
  variant: 'sm'
})

const classes = computed(() => {
  const base = ''

  const variants = {
    sm: 'max-w-18 min-w-18',
    md: '',
    lg: '',
    fullWidth: 'max-w-full'
  }

  return [
      base,
      variants[props.variant]
  ].join(' ')
})

</script>

<style scoped>

</style>
