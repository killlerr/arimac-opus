<template>
<div>
    <blockquote class="blockquote text-left bq">Overdue</blockquote>
    <footer class="blockquote-footer bqf">Lorem ipsum dolor sit amet consectetur</footer>
    <div>
        <CardFlip></CardFlip>
    </div>
    
</div>
</template>

<script>
import CardFlip from '~/components/CardFlip.vue'

export default {
    components:{
        CardFlip
    }
    
}
</script>

<style scoped>

.blockquote {
    margin-bottom: 0rem;
    font-size: 1.3rem;
    font-weight: bold;
}


.bqf{
    font-size: 19px;
}
</style>
