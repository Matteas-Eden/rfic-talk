<script setup lang="ts">
const props = defineProps({
    class: {
        type: String,
    },
    layoutClass: {
        type: String,
    },
});
</script>

<template>
    <div class="slidev-layout two-columns-with-header w-full h-full center" :class="props.layoutClass">
        <div class="flex flex-col items-center justify-center" :class="props.class">
            <slot />
        </div>

        <div class="grid grid-cols-2 px-16">
            <div class="col-left" :class="props.class">
                <slot name="left" />
            </div>

            <div class="col-right justify-self-end" :class="props.class">
                <slot name="right" />
            </div>
        </div>
    </div>
</template>