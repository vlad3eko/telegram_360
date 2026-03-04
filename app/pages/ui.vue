<template>
  <div>
    <NuxtLink to="/">main page</NuxtLink>
    <div class="block">
      <div class="block-el">
        <h4>Кнопки:</h4>
        <Button variant="primary">
          Primary
        </Button>
        <Button variant="inverse">
          Inverse
        </Button>
        <Button variant="primary" :icon="true">
          Primary Icon
        </Button>
        <Button variant="inverse" :icon="true" direction="inverse">
          Inverse Icon
        </Button>
        <Button variant="disable">
          disable
        </Button>
      </div>
    </div>
    <div class="block">
      <div class="block-el">
        <h4>Карточки:</h4>
        <Card
            :card-header-img="imgSrc"
            card-header-title="Описание карточки"
            card-header-status="Статус"
            card-title="заголовок"
            card-sub-title="под заголовок"
            :card-sub-image="imgSubDescription"
            card-sub-description="описание"
            card-trigger="кнопка"/>
        <Card
            :card-header-img="imgSrcGhost1"
            card-header-title="Описание карточки"
            card-header-status="Статус"
            card-title="заголовок"
            card-trigger="кнопка"/>
        <Card
            :card-header-img="imgSrcGhost2"
            card-header-title="Описание карточки"
            card-header-status="Статус"/>
      </div>
    </div>
    <div class="block">
      <div class="block-el">
        <h4>Inputs:</h4>
        <Inputs type="text"/>
        <Inputs type="email" :disabled="true"/>
        <Inputs type="password"/>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>

import Button from "~/components/UI/button/Button.vue";
import Card from "~/components/UI/сard/Card.vue";
import Inputs from "~/components/UI/inputs/Inputs.vue";

const imgSrc = 'https://images.wondershare.com/recoverit/article/2020/09/what-is-an-sd-card-3.jpg'
const imgSrcGhost1 = 'https://i.etsystatic.com/24358244/r/il/ff9f77/4792398603/il_570xN.4792398603_19hw.jpg'
const imgSrcGhost2 = 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQfYdweAGbTGl6xBNJqQF3IQYos7LrtdTNhVA&s'
const imgSubDescription = 'https://mainfin.ru/images/cryptoCurrency/eth.png'

</script>

<style scoped>

</style>
