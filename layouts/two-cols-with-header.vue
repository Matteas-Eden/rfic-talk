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

        <div class="grid grid-cols-2 gap-x-10 px-16">
            <div class="col-left justify-self-center" :class="props.class">
                <slot name="left" class="max-w-[50%]" />
            </div>

            <div class="col-right justify-self-center" :class="props.class">
                <slot name="right" class="max-w-[50%]" />
            </div>
        </div>
    </div>
</template>