<template>
    <div class="absolute w-full bg-red bg-opacity-30 h-screen top-0 left-0 flex justify-center px-8">
        <div class="p-4 bg-black mt-32 max-w-screen-md">
            <slot />
            <button class="text-black mt-8 bg-primary-color py-2 px-6">Close</button>
        </div>
    </div>
</template>

<script setup>

</script>

