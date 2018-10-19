<template>
    <!-- flip-container >> this is the flipping container -->
    <div class="flip-container">   


    <!-- Vue Flip -->
    <div>

                <transition name="flip" mode="out-in">
                    <component :is="mode" @answered="mode='appAnswer'" @confirmed="mode = 'appQuestion'"></component>
                </transition>


    </div>
    <!-- Vue Flip -->

</div>
</template>

<script>
import CardFront from '../components/CardFront.vue'
import CardBack from '../components/CardBack.vue'

export default {
    data() {
        return {
            mode: 'app-question'
        }
    },
    components:{
            appQuestion: CardFront,
            appAnswer: CardBack
    }
}
</script>


<style>

/* entire container, keeps perspective */
.flip-container {
	perspective: 1000px;
}


/*Vue Flip */


    .flip-enter {
        /*transform: rotateY(0deg);*/
    }

    .flip-enter-active {
        animation: flip-in  0.3s ease-out forwards;
    }

    .flip-leave {
        /*transform: rotateY(0deg);*/
    }

    .flip-leave-active {
        animation: flip-out 0.3s ease-out forwards;
    }

    @keyframes flip-out {
        from {
            transform: rotateY(0deg);
        }
        to {
            transform: rotateY(90deg);
        }
    }

    @keyframes flip-in {
        from {
            transform: rotateY(90deg);
        }
        to {
            transform: rotateY(0deg);
        }
    }



/*Vue Flip */




</style>

