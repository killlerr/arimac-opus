<template>
    <div class="input-field">
        <input
            class="form-control-opus mt-4"
            :placeholder="placeholder"
            :value="value"
            @change="$emit('input', $event.target.value)">
    </div>
</template>


<script>
export default {
    props: ['placeholder', 'value'],
    // computed: {
    //     inputEvent:function(e) {
    //         this.$emit('inputEvent', e); 
    //     }
    // }
}
</script>

<style>

.form-control-opus{

    width: 100%;
    font-family:sans-serif;
    /* text-transform: uppercase; */
    border-style: none;
    border-radius: 0;
    padding: 1.5rem;
    font-size: 11px;
    letter-spacing: 1px;

}

.form-control-opus:focus{
    /* border-left: 0.5rem solid #ff5a4e */
}

</style>

