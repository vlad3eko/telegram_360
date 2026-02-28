<template>
  <div class="flex flex-col gap-5 w-max m-5">
   <Button variant="primary">
      Primary
   </Button>
    <Button variant="inverse">
      Кнопка
    </Button>
    <Button variant="primary" :primary-with-icon-right="true">
      Кнопка
    </Button>
    <Button variant="inverse" :inverse-with-icon-left="true">
      Кнопка
    </Button>
    <Button variant="primary">
      Кнопка
    </Button>
  </div>
</template>

<script lang="ts" setup>


import Button from "~/components/UI/button/Button.vue";

const ts: string = 'ts Lang enable'
</script>

<style scoped>

</style>
