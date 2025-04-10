<template>
    <div class="px-4">
        <Header :navigation="navigation" />
    </div>
</template>

<script setup>
    import Header from './components/Header.vue'

    const navigation = [
        'Home',
        'Categories',
        'My Collections',
        'Blog',
    ]

    // localStorage.setItem('user', 'alina')
    // localStorage.getItem('user', 'alina')
</script>

