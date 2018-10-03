<template>

    <b-button class='btn btn-base' :label="label" @click="onClick">
         {{label}}
    </b-button>

</template>

<script>
export default {
    props:['label','onClick'],
    // event: 'doSomething'
}
  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.btn-base{
    background: #e74132;
    color: #ffffff;
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
    background: #e74132;
    color: #ffffff;
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
    background: #b72315;
    color: #f0f0f0;
}

.btn:active{
    transform: translateY(-1px);
    background: #e74132;
    color: #ffffff;
}
</style>
