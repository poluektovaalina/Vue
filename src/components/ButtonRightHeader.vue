<template>
    <div>
        <button class ="py-[12px] px-[28px] rounded-[5px] text-[#FDF5FF] font-bold hover:shadow-[0_0_15px_#FF6E30] cursor-pointer" :class = "backgroundColor">{{ textButton }}</button>
    </div>
</template>

<script setup>
    defineProps({
        backgroundColor: String,
        textButton: String
    })
</script>

<style lang="scss" scoped>

</style>