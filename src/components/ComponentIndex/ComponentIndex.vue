<template>
    <div class="container-fluid">

        <!-- Title h1 -->
        <div class="row bg-dark py-3">
            <h1 class="text-light text-center">{{ title }}</h1>
        </div>

        <!-- Content -->
        <div class="container p-3">

            <!-- subTitle -->
            <div class="col-10 mx-auto">
                <h2 class="">{{ subTitle }}</h2>
            </div>

            <!-- form task -->
            <formTask v-on:addTask="addTask"></formTask>

            <!-- display tasks -->
            <resultTasks v-bind:tasks="tasks" v-on:deleteTask="deleteTask"></resultTasks>
       
        </div>
    </div>
</template>


<script>
    import FormTask from '../FormTask.vue';
    import ResultTasks from '../ResultTasks.vue';

    export default {
        name: 'ComponentIndex', 
        data: function() {
            return {
                title: 'La To-Do Liste !', 
                subTitle: 'Rentrez vos choses à faire.',
                tasks: [],
            }
        }, 
        components: {
            'formTask': FormTask,
            'resultTasks': ResultTasks
        }, 
        methods: {
            addTask: function(task) {
                this.tasks.push(task)
            },
            deleteTask(index) {
                this.tasks.splice(index, 1)
            },
        }
    }

</script>


<style scoped src="./ComponentIndex.css"></style>