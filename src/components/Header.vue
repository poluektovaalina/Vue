<template>
    <div class="w-full my-0 max-w-[1224px] mx-auto">
        <div class="flex items-center justify-between py-[30px]">
            <div class="logo text-white flex items-center gap-[12px]">
                <img src="../assets/logo.svg" alt="">
                <span class="font-bold">antools.</span>
            </div>
            <nav class="flex gap-[42px]  font-16 text-[#9A9DA0] font-bold">
                <Navigation v-for="(nav, index) in navigation" :key="index" :nav="nav" />
            </nav>
            <div class=" flex gap-4">
                <ButtonRightHeader v-if="condition" backgroundColor="bg-[]" textButton="Login" />
                <ButtonRightHeader v-if="condition" backgroundColor="bg-[#FF6E30]" textButton="Sign up" />
                <ButtonRightHeader v-if="!condition" backgroundColor="bg-[#FF6E30]" textButton="Exit" />
            </div>
        </div>
    </div>
</template>

<script setup>
    defineProps({
        navigation: Array,
    })
    
    let condition = true
    const user = localStorage.getItem('user')
    if( user){
        condition = false;
        
    }else{
        condition = true;
    }
    
    import ButtonRightHeader from './ButtonRightHeader.vue';
    import Navigation from './Navigation.vue';
</script>

<style lang="scss" scoped>

</style>