<template>
    <div>
        about
    </div>
    <div>
        <button @click="enableCustomLayout">Update layout</button>
    </div>
</template>

<script setup>
    // definePageMeta({
    //     layout: 'another'
    // })
    const enableCustomLayout = () => {
        setPageLayout('another');
    }
</script>