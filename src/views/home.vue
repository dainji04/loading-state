<template>
    <div>
        <div v-if="loading" class="loading-screen">
            <Loading />
        </div>
        <div class="home">
            <h1>this is home page</h1>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import Loading from '@/components/loading.vue';
const loading = ref(true);

const load = setTimeout(() => {
    loading.value = false;
}, 4000);
</script>

<style>
.loading-screen {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    font-size: 24px;
}
</style>
