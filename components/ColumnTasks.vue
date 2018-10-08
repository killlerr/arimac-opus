<template>

<div>
    <blockquote class="blockquote text-left bq">Tasks</blockquote>
    <footer class="blockquote-footer bqf">Lorem ipsum dolor sit amet consectetur</footer>
    
                    <div class="row row-gap">
                        <ButtonAddNewTask label="Add new task card" :onClick="doSomething"></ButtonAddNewTask>
                        
                    </div>
    
</div>

</template>

<script>
import ButtonAddNewTask from '~/components/ButtonAddNewTask.vue'


export default {
    components: {
        ButtonAddNewTask

    },
    methods: {
        doSomething: function () {
            // <nuxt-link to="appTasks"></nuxt-link>
            
        }
    }
}


</script>

<style scoped>

.blockquote {
    margin-bottom: 0rem;
    font-size: 1.4rem;
    font-weight: bold;
}


.bqf{
    font-size: 19px;
}
</style>
