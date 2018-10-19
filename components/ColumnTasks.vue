<template>

<div>
    <div class="py-3">
    <blockquote class="blockquote text-left bq">Tasks</blockquote>
    <footer class="blockquote-footer bqf">Lorem ipsum dolor sit amet consectetur</footer>
    </div>

    
        <div class="pb-2 pt-2">
            <Reusable-button label="Add new task card" class="btn-add-new-task" :onClick="doSomething" v-bind:style="{'background-color':btnBgColor, color:btnColor}"></Reusable-button>
        </div>
        <div class="margin-top-from-btn">
            <CardFlip></CardFlip>
            <CardFlip></CardFlip>
        </div>

                    
</div>

</template>

<script>
import ReusableButton from '~/components/ReusableButton.vue'
import CardFlip from '~/components/CardFlip.vue'

export default {

    components: {
        CardFlip,
        ReusableButton

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
    font-size: 1.3rem;
    font-weight: bold;
}


.bqf{
    font-size: 19px;
}



.btn-add-new-task{
    border-radius: 0.25rem;
    box-shadow: 0 0.05rem 0.2rem 0 rgba(0, 0, 0, 0.2);
    width: 100%;
    background-color: #ffffff;
    color:#80818cfa;
}

</style>
