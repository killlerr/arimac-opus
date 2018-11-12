<template>
    <div class="input-field">
        <input
            v-model="value"
            class="form-control-opus mt-4"
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

.form-control-opus{

    width: 100%;
    font-family:sans-serif;
    text-transform: uppercase;
    border-style: none;
    border-radius: 0;
    padding: 1.5rem;
    font-size: 11px;
    letter-spacing: 1px;

}

.form-control-opus:focus{
    /* border: 0 0 0 1rem solid #ff5a4e */
    border-left: 10px;
    border-color: 
dddd
}

</style>

