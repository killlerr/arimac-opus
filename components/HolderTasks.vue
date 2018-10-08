<template>
    <div class="row">
        <div class="col-md-4 d-flex justify-content-center">
           <Column-tasks></Column-tasks>
        </div>        
        <div class="col-md-4 d-flex justify-content-center">
           <Column-overdue></Column-overdue>
        </div>
        <div class="col-md-4 d-flex justify-content-center">
           <Column-completed></Column-completed>
        </div>
    </div>
</template>

<script>
import ColumnCompleted from "~/components/ColumnCompleted.vue"
import ColumnOverdue from "~/components/ColumnOverdue.vue"
import ColumnTasks from "~/components/ColumnTasks.vue"

export default {
    components:
    {
        ColumnCompleted,
        ColumnOverdue,
        ColumnTasks
    }
    
}
</script>

<style scoped>

</style>
