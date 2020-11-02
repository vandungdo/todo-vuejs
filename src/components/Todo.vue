<template>
    <div class="todo">
        <div class="container">
            <div class="row align-items-center">
                <div class="form-group mx-sm-3 mb-2">
                    <label for="inputPassword2" class="sr-only">Please add task</label>
                    <input type="text" class="form-control" id="inputPassword2" placeholder="task" v-model="newTask">
                </div>
                
                
                <button @click="todos.push({task: newTask, finish: false})" type="submit" class="btn btn-primary mb-2">Add</button>
            </div>
                <br>
            
                <div v-for= "(todo,index) in todos" :key="index">
                    <div class="row align-items-center">
                        <div class="input-group-text">
                            <input type="checkbox" v-model="todo.finish">
                            <span :class="{finished: todo.finish}"> {{ todo.task }} </span>
                        </div>
                        
                    </div>
                </div>
            
            
        </div>
    </div>
</template>

<script>
export default {
    name: 'Todo',
    data() {
        return {
            newTask: '',
            todos: [
                
            ],
        }
    }
}
</script>

<style scoped>
.finished {
    text-decoration: line-through;
}
</style>