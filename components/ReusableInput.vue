<template>
    <div class="input-field">
        <input
            class="input-reusable mt-4"
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

.input-reusable{

    width: 100%;
    font-family:sans-serif;
    /* text-transform: uppercase; */
    border-style: none;
    border-radius: 0;
    padding: 1.5rem;
    font-size: 11px;
    letter-spacing: 1px;

}

.input-reusable:focus{
    border-left: 0.4rem solid #ff5a4e;
    outline: 0;
}

</style>

