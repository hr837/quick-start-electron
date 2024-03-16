<template>
    <div class="app-counter">
        <el-button @click="onIncrease" icon="plus">增加</el-button>
        <div class="app-counter_text">Count is : {{ counter }}</div>
        <el-button @click="onDecrease" icon="minus">减少</el-button>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const counter = ref(1);

const onIncrease = () => counter.value += 1;
const onDecrease = () => counter.value -= 1;

</script>

<style>
.app-counter {
    display: flex;
    align-items: center;
}

.app-counter_text {
    min-width: 120px;
    text-align: center;
}
</style>