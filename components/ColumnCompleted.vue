<template>
<div>
    <blockquote class="blockquote text-left bq">Completed</blockquote>
    <footer class="blockquote-footer bqf">Lorem ipsum dolor sit amet consectetur</footer>
    <BaseCard></BaseCard>
    <BaseCard></BaseCard>
    <BaseCard></BaseCard>
</div>
</template>

<script>
import BaseCard from '~/components/BaseCard.vue'
export default {
    components:{
        BaseCard
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
