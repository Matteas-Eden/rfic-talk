<template>
  <div class="slidev-layout section">
    <div class="grid grid-cols-2 justify-between items-center">
        <div>
            <slot />
        </div>
        <div>
            <slot name="content" />
        </div>
    </div>
  </div>
</template>