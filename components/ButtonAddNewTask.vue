<template>

    <b-button class='btn btn-base' :label="label" @click="onClick">
         {{label}}
    </b-button>

</template>

<script scoped>
export default {
    props:['label','onClick'],
    // event: 'doSomething'
}
  
</script scoped>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.btn-base{
    background: #af6f6f;
    color: #80818cfa;
    border-radius: 0px;
    text-transform: uppercase;
    font-size: 11px;
    padding: 20px;
    width:100%;
    font-family:sans-serif;
    letter-spacing: 1px;
    font-weight: bold;
    display: inline-block;
    border-style: none;
}

.btn:link,
.btn:visited{
    background: #7e2323;
    color: #80818cfa;
    border-radius: 0px;
    text-transform: uppercase;
    font-size: 11px;
    padding: 20px;
    width:100%;
    font-family:sans-serif;
    letter-spacing: 1px;
    font-weight: bold;
    display: inline-block;
    border-style: none;
}

.btn:hover{
    transform: translateY(-1px);
}

.btn:active{
    transform: translateY(-1px);
}
</style>
