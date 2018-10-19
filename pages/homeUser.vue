<template>
    <div>
        <Header></Header>
        <tabs></tabs>
    </div>

</template>

<script>
import Header from '~/components/Header.vue'
import Tabs from '~/components/Tabs.vue'

export default {
        components: {
        Header,
        Tabs
    }
}
</script>

<style>

.bg{
    background-color: aquamarine;
}

.bg-test{
    background-color:red;
}
</style>
