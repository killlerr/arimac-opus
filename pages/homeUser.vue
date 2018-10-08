<template>
    <div>
        <Header></Header>
        <!-- <Header-second></Header-second> -->
        <tabs></tabs>
    </div>

</template>

<script>
import Header from '~/components/Header.vue'
import HeaderSecond from '~/components/HeaderSecond.vue'
import HolderTasks from '~/components/HolderTasks.vue'
import Tabs from '~/components/Tabs.vue'

export default {
        components: {
        Header,
        HeaderSecond,
        HolderTasks,
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
