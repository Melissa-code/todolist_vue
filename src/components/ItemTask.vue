<template>
    <li class="card p-3 my-2">
        <span class="row d-flex align-items-center">
            <!-- task -->
            <span class="col-md-11">
                {{ task }}
            </span>
            <!-- delete button -->
            <span class="col-md-1">
                <button v-on:click="$emit('delete')" class="deleteBtn">
                    x
                </button>
            </span>
        </span>
    </li>
</template>


<script>
    export default {
        name: 'ItemTask',
        props: {
            task: {
            type: String,
            required: true,
            },
        },
    }
</script>

<style>
    .deleteBtn {
        border: 1px solid red;
        background-color: red;
        color: white; 
        border-radius: 5px;
        padding-bottom: 5px;
    }
</style>