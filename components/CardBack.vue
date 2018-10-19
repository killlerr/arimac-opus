<template>
    <div>
        <div class="pb-2 pt-2">
        <b-card class="card-back" v-bind:style="{'background-color':bgColor}" @click="onNextQuestion">
            <div class="col">
            <div class="row">
                <div class="col-6">
                    <h3>Completed Card</h3>
                    <p><small>This line of text is meant to be treated as fine print.</small></p>
                </div>
                <div class="col-6">
                    <b-button class="filter-button" :class="{toggled: isToggled}" @click="isToggled = !isToggled">
                        <slot>toggle</slot>
                    </b-button>                  
                </div>
            </div>
            </div>
        </b-card>
        </div>
    </div>



</template>

<script>
export default {
    data(){
        return{
            bgColor: '#ff5a4e',
            isToggled: false
        }
    },
    methods: {
            onNextQuestion() {
                this.$emit('confirmed');
            }
        }
    
}
</script>

<style>

.card-body {
    width: 100%;
    height: 100%;
    padding: 0px;
}

.card-back{

    width: 100%;
    border-radius: 0.25rem;
    box-shadow: 0 0.05rem 0.2rem 0 rgba(0, 0, 0, 0.2);
    word-wrap: break-word;
    height: 9.99rem;
}

</style>

