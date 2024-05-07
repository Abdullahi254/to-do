<template lang="">
    <div class="w-full bg-white shadow-xl shadow-green-300 rounded px-8 pt-6 pb-8 mb-4">
        <ul v-for="(item, index) in list" class="space-y-4 text-sm list-disc">
            <TodoItem :item="item"/>
        </ul>
        <InputTodo @todo="addTodo"/>
    </div>
</template>
<script setup>
    const list = ref(["Buy Shirt", "Buy Trousers", "Buy Shoes", ])
    onMounted(()=>list)
    const addTodo = (val)=>{
        console.log(val)
        list.value.push(val)
    }
</script>
<style lang="">
    
</style>