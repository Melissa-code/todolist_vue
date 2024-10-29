<template>
    <ul class="col-10 mx-auto my-4">
        <itemTask 
            v-bind:key="index" 
            v-bind:task="task" 
            v-for="(task, index) in tasks"
            @delete=" ()=> $emit('deleteTask', index)">
        </itemTask>
    </ul>
</template>


<script>
    import ItemTask from './ItemTask.vue';

    export default {
        name: 'ResultTasks',
        data: function() {
            return {
               
            }
        },
        components: {
            'itemTask': ItemTask
        },
        props: {
            tasks: {
                type: Array,
                required: true,
            },
        }
    }
</script>

<style></style>