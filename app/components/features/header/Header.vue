<template>
  <Menu/>
  <Section class="gap-10 bg-background" :direction-row="true">
    <div class="container grid grid-cols-3 gap-5">
      <div class="border flex gap-5 flex-col justify-between col-start-1">
        <span class="border-accent border w-50 max-h-0 col-start-1"/>
        <h1 class="leading-14">Discover And Create NFTs</h1>
        <p class="text-muted-foreground">Discover, Create and Sell NFTs On Our NFT Marketplace With Over Thousands Of
          NFTs And Get a
          <span class="font-bold text-accent-foreground">$20 bonus</span>.
        </p>
        <div class="flex gap-7">
          <Button variant="primary">Explore More</Button>
          <Button variant="inverse">create NFT</Button>
        </div>
      </div>
      <div class="border flex justify-between col-start-1">
        <div class="leading-7">
          <Counter count="430" letter="K+" class="text-3xl font-bold"/>
          <p class="text-muted-foreground">Art Works</p>
        </div>
        <div class="leading-7">
          <Counter count="430" letter="K+" class="text-3xl font-bold"/>
          <p class="text-muted-foreground">Art Works</p>
        </div>
        <div class="leading-7">
          <Counter count="430" letter="K+" class="text-3xl font-bold"/>
          <p class="text-muted-foreground">Art Works</p>
        </div>
      </div>
      <div class="border col-start-2 col-span-2 row-span-3 row-start-1">
        <Swiper/>
      </div>
    </div>
  </Section>
</template>

<script lang="ts" setup>

import Button from "~/components/UI/button/Button.vue";
import Section from "~/components/features/Section.vue";
import Counter from "~/components/UI/Counter.vue";
import Menu from "~/components/features/header/Menu.vue";
import Swiper from "~/components/UI/Swiper.vue";
</script>

<style scoped>

</style>
