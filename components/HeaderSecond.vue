<template>
    <div>
<b-navbar toggleable="md" type="light" variant="dark" class="navbar pb-1">

    <!-- Right aligned nav items -->
    <b-navbar-nav class="m-auto mx-2">
          <b-nav-item href="homeUser/holderTasks" class="mx-3 pt-1 nav-b">Task</b-nav-item>
          <b-nav-item href="homeUser/holderAttendence" class="mx-3 pt-1 nav-b">Attendence</b-nav-item>
    </b-navbar-nav>

 
</b-navbar>

    </div>
</template>

<script>
import HolderTasks from '../components/HolderTasks'
import HolderAttendence from '../components/HolderAttendence'
export default {
    components:{
        HolderTasks,
        HolderAttendence
    }
}
</script>

<style scoped>



html{
    font-size: 62.5%;
}

.navbar{
    background-color: #ffffff!important;
    box-shadow: 0px 1px 3px #efeeee, 0px 1px 2px #bfbfbf;
    padding: 0;
}

.nav-b,.nav-link{
    color:#80818cfa !important;
    font-weight: bold;
    height: 3rem;
    text-align: center;
    border-bottom: 5px solid transparent;
    
}

.nav-link:hover, .nav-link:active{
    border-bottom: 5px solid red;
}
</style>
