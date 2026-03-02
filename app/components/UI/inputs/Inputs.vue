<template>
  <input :type="props.type" :class="[isDisabled, classes]" :placeholder="placeholders" :disabled="disabled">
</template>

<script lang="ts" setup>

interface IInputs {
  type:
  | 'text'
  | 'password'
  | 'checkbox'
  | 'time'
  | 'email'
  | 'file'
  | 'radio'
  | 'search'
  | 'reset'
  | 'submit'
  disabled?: boolean
}

const props = withDefaults(defineProps<IInputs>(), {
  disabled: false
})

const classes = 'bg-card p-2 rounded-2xl w-full min-w-15 border'
const isDisabled = props.disabled ? 'bg-foreground/10 cursor-not-allowed' : ''

const placeholders = computed(() => {
  const types = {
    text: 'поле',
    password: 'пароль',
    checkbox: '',
    time: '',
    email: 'емаил',
    file: '',
    radio: '',
    search: 'Ctrl K',
    reset: '',
    submit: '',
  }

  return [
      types[props.type]
  ].join(' ')
})

</script>

<style scoped>

</style>
