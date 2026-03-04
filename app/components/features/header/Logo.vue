<template>
  <div class="flex items-center gap-2">
    <NuxtImg :class="classes" src="/logo.png"/>
      <span v-if="props.logoShowName" class="text-primary/80 text-3xl font-bold max-sm:hidden">TG<Counter count="360" class="text-5xl"/></span>
  </div>
</template>

<script lang="ts" setup>

import Counter from "~/components/UI/Counter.vue";

interface ILogo {
  logoVariant?: 'sm' | 'md' | 'lg' | 'fullWidth'
  logoShowName?: boolean
}

const props = withDefaults(defineProps<ILogo>(), {
  logoVariant: 'sm',
  logoShowName: true
})

const classes = computed(() => {
  const base = 'transparent'

  const variants = {
    sm: 'max-w-18 min-w-18',
    md: '',
    lg: '',
    fullWidth: 'max-w-full'
  }

  return [
      base,
      variants[props.logoVariant]
  ].join(' ')
})

</script>

<style scoped>

</style>
