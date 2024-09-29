<script setup lang="ts">
  import IconWeb from '~icons/mdi/web'
  import IconMail from '~icons/mdi/email'
  import IconPersonGroup from '~icons/mdi/person-group'
  import IconTheatre from '~icons/mdi/theatre'
  import IconKarate from '~icons/mdi/karate'

  const props = defineProps<{
    imageSrc?: string
    helloMsg?: string
    name?: string
    job?: string
    improv?: string
    karate?: string
    website?: string
    email?: string
  }>()
</script>

<template>
  <div class="slidev-layout about-me p-0">
    <div class="flex h-full items-center justify-between">
      <img class="w-100 h-100 ml-20 flex rounded-full" :src="imageSrc">
      </img>
      <!-- <div class="w-100 h-100 ml-20 flex rounded-full" :style="style">
      </div> -->
      <div class="w-1/2 flex flex-col justify-between items-end px-8 py-16">
        <h1 v-if="helloMsg" class="flex">{{ helloMsg }}</h1>

        <div class="flex flex-col justify-end items-end text-right py-16">
          <h2 class="font-extrabold">{{ name }}</h2>

          <div class="text-2xl space-y-2 mt-4">
            <p class="job"><icon-person-group class="mr-1" />{{ job }}</p>
            <p class="line-1"><icon-theatre class="mr-1" />{{ improv }}</p>
            <p class="line-2"><icon-karate class="mr-1" />{{ karate }}</p>
          </div>

          <div class="text-2xl space-y-2 mt-4">
            <p class="social social-1"><icon-web class="mr-1" />{{ website }}</p>
            <p class="social social-2"><icon-mail class="mr-1" />{{ email }}</p>
          </div>
        </div>
      </div>
    </div>

    <slot />
  </div>
</template>

