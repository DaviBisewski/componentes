<script setup>
import { ref, computed } from 'vue';
const props = defineProps(['title', 'content'])
const ShowBox = ref(false)
const textobotao = computed(() => ShowBox.value ? 'Esconder' : 'Mostrar')
</script>

<template>
    <div>
        <button @click="ShowBox =! ShowBox">{{ textobotao }}</button>
        <div v-if="ShowBox" class="expand-box">
            <h1>{{ props.title }}</h1>
            <p>{{ props.content }}</p>
        </div>
    </div>

</template>

<style scoped>
.expand-box {

    width: 300px;
    height: 100%;
    padding: 20px;
    border: 1px solid black;
    box-shadow: 2px 2px 2px 2px gray;
}
</style>