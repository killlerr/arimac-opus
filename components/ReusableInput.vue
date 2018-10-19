<template>
    <div class="input-field">
        <input
            v-model="value"
            class="form-control mt-4"
            :placeholder="placeholder"
            @v-on:keyup.enter="inputEvent">
    </div>
</template>


<script>
export default {
    props: ['placeholder', 'value'],
    computed: {
        inputEvent:function(e) {
            this.$emit('inputEvent', e); 
        }
    }
}
</script>

<style>

.form-control{

    width: 100%;
    font-family:sans-serif;
    text-transform: uppercase;
    border-style: none;
    border-radius: 0;
    padding: 1.9rem;
    font-size: 11px;
    letter-spacing: 1px;

}



</style>

