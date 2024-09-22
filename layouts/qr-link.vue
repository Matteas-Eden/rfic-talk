<script setup lang="ts">
import { computed } from 'vue'
import QRious from 'qrious'

const props = defineProps({
  url: {
    type: String,
    default: '',
  },
})

const qrcode = computed(() => {
  return new QRious({
    value: props.url,
    size: 300,
  }).toDataURL()
})
</script>

<template>
  <div class="slidev-layout center text-center">
    <slot />
    <div class="container mx-auto">
      <img
        :src="qrcode"
        alt="QR Code"
        class="w-m inline-block border-4 border-[#5EADF2]"
      >
    </div>
  </div>
</template>