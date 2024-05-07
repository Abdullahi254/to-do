<template>
  <div>
    <form class="rounded px-8 pt-6 pb-8 mb-4 w-full">
      <input required
        class="shadow appearance-none border border-red-500 rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline"
        id="text" type="text" v-model="text">
        <button class="text-black w-full hover:bg-green-700 hover:text-white text-sm bg-green-200 rounded-xl p-2"
          @click.prevent="createTodo">Add</button>
    </form>
  </div>
</template>

<script lang="ts" setup>
const emit = defineEmits(['todo'])
const text = ref('')
const createTodo = () => {
  emit('todo', text.value)
  text.value = ''
}
</script>

<style></style>
