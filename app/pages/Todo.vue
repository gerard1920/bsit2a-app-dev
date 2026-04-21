<template>
    <div>
        <h1>Todo List</h1>

        <v-card>
            <v-card-text>
                <v-data-table :items="todos" :headers="headers"></v-data-table>
            </v-card-text>
        </v-card>
    </div>
</template>


<script setup>
const headers = [
    { title: 'ID', key: 'id' },
    { title: 'Title', key: 'title' },
    { title: 'Completed', key: 'completed' }
]
const todos = ref([])

const getTodos = async () => {
    const data = await $fetch('https://jsonplaceholder.typicode.com/todos')
    todos.value = data
    console.log(data)
}

onMounted (() => {
    getTodos();
        

})

</script>