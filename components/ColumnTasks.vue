<template>

<div>
    <blockquote class="blockquote text-left bq">Tasks</blockquote>
    <footer class="blockquote-footer bqf">Lorem ipsum dolor sit amet consectetur</footer>
    
        <div>
            <CardModalNewTaskCard></CardModalNewTaskCard>
        </div>
        <div class="margin-top-from-btn">
            <CardFlip></CardFlip>
            <CardFlip></CardFlip>
        </div>

                    
</div>

</template>

<script>
import CardModalNewTaskCard from '~/components/CardModalNewTaskCard.vue'
import CardFlip from '~/components/CardFlip.vue'

export default {
    components: {
        CardFlip,

        CardModalNewTaskCard

    },
    methods: {
        doSomething: function () {
            console.log("Added New Card")
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

.btn-base{
    width: 180% !important;
}



.margin-top-from-btn{
    margin-top: 6.6rem;
}

</style>
