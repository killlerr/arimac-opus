<template>
<div>
<b-navbar toggleable="md" type="dark" variant="dark" class="navbar fixed-top">

  <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

  <b-navbar-brand href="homeUser"><img src="logo-opus-nav.jpg" class="logo-opus ml-3 my-3" alt="Responsive image"> </b-navbar-brand>
    <b-navbar-nav class="ml-auto 	">
          <div class="container d-flex justify-content-center d-none d-sm-block d-md-none">
        <b-nav-item href="profile">
        <div class="row no-gutters">
          <div class="col-6">
            <img src="img-profile-picture.jpeg" class="img-circle img-profile" alt="Cinque Terre">
          </div>
          <div class="col-6 flex-column name-box d-none d-sm-block">
            <div class="text-light mx-2 user-name">{{userName}}</div>
            <div class="text-secondary mx-2 user-power">{{userPower}}</div>
          </div>
        </div>
        </b-nav-item>
          </div>
    </b-navbar-nav>
  <b-collapse is-nav id="nav_collapse">

      <b-nav-form class="search-form mx-5">
        <b-form-input  id="input-large" size="sm" class="mr-sm-2" type="text" placeholder="Search Cards" style="font-family:Arial, FontAwesome" />
      </b-nav-form>

    <!-- Right aligned nav items -->
    <b-navbar-nav class="ml-auto mx-2 my-3 ">

          
          <b-nav-item href="messageArea" class="mx-3"><fa :icon="fas.faComments"  :style="{ color: '' }" class="fa-2x mt-2"/></b-nav-item>

      <b-nav-item-dropdown right>
        <!-- Using button-content slot -->
        <template slot="button-content">
          <em class="mx-3"><fa :icon="fas.faEllipsisV"  :style="{ color: '' }" class="fa-2x mt-2 mr-4" /></em>
          
        </template>
        <b-dropdown-item href="settings">Settings</b-dropdown-item>
        <b-dropdown-item href="/">Signout</b-dropdown-item>
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
    data(){
      return{
        userName:'Indika',
        userPower: 'User'
      }
    },
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






.navbar{
  padding: 0;
  padding-top: 0.1rem;
  background-color: #2a2e43 !important;
  width: 100vh;
  max-width: 100%;
  min-width: 100%;
}

.logo-opus{
      height: 2.8rem;
      width: auto;    
}

.img-profile{
      height: 3rem;
      width: auto;   
      align-content: center;
      border-radius: 50%;
      margin-bottom: 5px;
  
}

.fa-size{
      height: 1.6rem;
      width: auto; 
}

.dropdown-toggle::after {
    display:none;
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


.user-name{
  font-size: 16px;
  font-weight: bolder;
  text-align:top;
}

.user-power{
  font-size: 14px;
  font-weight: bold
}

.name-box{
  margin-bottom: 4px;
  vertical-align: top
}

.nav-link{
  padding: 0;
}

</style>
