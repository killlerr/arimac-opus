<template>  
<div>
<b-card no-body class="img-cover">
  <b-tabs card>
    <b-tab title="Task" active class="px-2">
      <holder-tasks></holder-tasks>
    </b-tab>
    <b-tab title="Attendence" class="px-1">
      <holder-attendence></holder-attendence>
    </b-tab>
  </b-tabs>
</b-card>
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

<!-- Styles are used for tab animation, which is open for customization and optional -->
<style>


.card-header{
    background-color: #ffffff!important;
    box-shadow: 0px 1px 3px #efeeee, 0px 1px 2px #bfbfbf;
    padding: 0.5rem;
    border: 0;
    height: auto;
}

.nav-tabs .nav-link.active, .nav-tabs .nav-item.show .nav-link {
    color: #495057;
    background-color: #fff;
    border-width: 0;
    border-bottom: 5.5px solid #ff5a4e;
    
    
}

.nav-link{
    color:#80818cfa !important;
    font-weight: bold;
    height: 3rem;
    text-align: center;
    border-bottom: 5px solid transparent;
    text-align: center;
    font-size: 1rem;
    
}

.nav-tabs .nav-link:hover, .nav-tabs .nav-link:focus {
    border-width: 0;
    border-bottom: 5.5px solid #ff5a4e;
}

.card-header-tabs {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: -0.45rem;
    border-bottom: 0;
}

.tab-content{


}




.card-body:after {

}

/*Background*/


</style>



