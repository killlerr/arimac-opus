<template>
<div class="bg-wrap">
 
                    
                    <div class="row row-gap">
                        <Base-button label="Login" :onClick="doSomething"></Base-button>
                    </div>
    
</div>

</template>

<script>
import BaseButton from '~/components/BaseButton.vue'


export default {
    components: {
        BaseButton,

    },
    methods: {
        doSomething: function () {
            // <nuxt-link to="appTasks"></nuxt-link>
            
        }
    }
}
</script>


<style>




</style>
