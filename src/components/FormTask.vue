<template>
    <div class="col-10 mx-auto">
        <form>
            <!-- input for a task -->
            <div class="form-group my-3">
                <label for="task" >Action</label>
                <input v-model="task" type="text" id="task" class="form-control" placeholder="Ajouter une tâche">
            </div>

            <!-- submit button -->
            <button v-on:click.prevent="sendData" class="btn btn-primary my-2">
                Créer une tâche
            </button>
        </form>
    </div>
</template>


<script>
    export default {
        name: 'FormTask',
        data: function() {
            return {
                task: '',
            }
        },
        methods: {
            sendData: function() {
                if (this.task.trim() !== '') {
                    this.$emit('addTask', this.task)
                    this.task = ''
                }
            }
        }
    }
</script>

<style></style>