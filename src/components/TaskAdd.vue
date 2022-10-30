<script setup lang="ts">
import { ref } from "vue";

const emit = defineEmits<{
    (eventName: "add", newTaskTitle: string): void;
}>();

const newTaskTitle = ref("");

const addTask = () => {
    // テキストが1文字以上のとき、イベントを起こす
    if (newTaskTitle.value.length > 0) {
        emit("add", newTaskTitle.value);
        newTaskTitle.value = "";
    }
};
</script>

<template>
    <form action="" class="form-floating">
        <input type="text" v-model="newTaskTitle" class="form-control mt-4" placeholder="Add Task" @keydown.enter.prevent="addTask()" />
        <label for="">Add Task</label>
    </form>
</template>
