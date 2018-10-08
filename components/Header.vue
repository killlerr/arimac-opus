<template>
<div>
<b-navbar toggleable="md" type="dark" variant="dark" class="navbar py-0.5">

  <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

  <b-navbar-brand href="#"><img src="logo-opus-nav.jpg" class="logo-opus ml-3" alt="Responsive image"> </b-navbar-brand>

  <b-collapse is-nav id="nav_collapse">

      <b-nav-form class="search-form">
        <b-form-input  id="input-large" size="sm" class="mr-sm-2" type="text" placeholder="Search Cards" style="font-family:Arial, FontAwesome" />
      </b-nav-form>

    <!-- Right aligned nav items -->
    <b-navbar-nav class="ml-auto mx-2">
          <b-nav-item href="#" class="mx-3"><fa :icon="fas.faUserAlt"  :style="{ color: '' }"  class="fa-size"/></b-nav-item>
          <b-nav-item href="#" class="mx-3"><fa :icon="fas.faComments"  :style="{ color: '' }" class="fa-size"/></b-nav-item>

      <b-nav-item-dropdown right>
        <!-- Using button-content slot -->
        <template slot="button-content">
          <em class="mx-3"><fa :icon="fas.faEllipsisV"  :style="{ color: '' }" class="fa-size" /></em>
          
        </template>
        <b-dropdown-item href="#">Profile</b-dropdown-item>
        <b-dropdown-item href="#">Signout</b-dropdown-item>
      </b-nav-item-dropdown>
    </b-navbar-nav>

  </b-collapse>
</b-navbar>

   

</div>
</template>

<script>

// fontawesome: {
//   component: 'fa'
// }

import { fas } from '@fortawesome/free-solid-svg-icons'
  import { faGithub } from '@fortawesome/free-brands-svg-icons'
  export default {
    computed: {
      fas () {
         return fas
      },
      faGithub () {
         return faGithub
      }
    },
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


html{
    font-size: 62.5%;
}



.navbar{
  padding: 0;
  padding-top: 0.1rem;
  background-color: #2a2e43 !important;
}

.logo-opus{
      height: 2.8rem;
      width: auto;    
}

.fa-size{
      height: 1.6rem;
      width: auto; 
}

/* Placeholder */

.mr-sm-2{
    font-size: 16px;
    padding-right: 4rem;
    padding-top: 1.25rem;
    padding-bottom: 1.25rem;
    font-family:sans-serif;
    font-variant-position: normal;
    display: inline-block;
    background-color: #5d6177;
    color: #9f9f9f;
    border-style: none;
    border-radius: 0;
    vertical-align: top;
}

.mr-sm-2::-webkit-input-placeholder { /* Chrome/Opera/Safari */
    color: #afafaf;
    opacity: 0.8;
    margin-left: 5rem;
}
.mr-sm-2::-moz-placeholder { /* Firefox 19+ */
    color: #afafaf;
    opacity: 0.8;
}
.mr-sm-2:-ms-input-placeholder { /* IE 10+ */
    color: #afafaf;
    opacity: 0.8;
}
.mr-sm-2:-moz-placeholder { /* Firefox 18- */
    color: #afafaf;
    opacity: 0.8;
}

.search-form input[type=text]{
  padding-left: 2rem;
  font-family: FontAwesome;
}

/* Placeholder */



</style>
