<template>
    <Transition>
        <div 
    v-show="modalActive"
    class="absolute w-full bg-opacity-30 h-screen top-0 left-0 flex justify-center px-8">
       <Transition>
        <div 
        v-if="modalActive"
        class="p-4 bg-secondary-color self-start mt-32 max-w-screen-md">
            <slot />
            <button class="text-white rounded-full mt-8 bg-primary-color py-2 px-6"
            @click="$emit('close-modal')"
            >Close</button>
        </div>
       </Transition>
    </div>
    </Transition>
</template>

<script setup>
defineEmits(["close-modal"])
defineProps({
    modalActive: {
        type: Boolean,
        default: false,
    }
})
</script>

