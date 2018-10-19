<template>
  <div>
    <b-navbar toggleable="md" type="dark" variant="dark" class="header py-2">
      <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
      <b-navbar-brand href="homeUser"><img src="logo-opus-nav.jpg" class="logo-opus ml-3" alt="Responsive image"> </b-navbar-brand>
      
      
      <b-collapse is-nav id="nav_collapse">
      <b-nav-form class="search-form mx-5">
        <b-form-input  id="input-large" size="sm" class="input-search m-2" type="text" placeholder="Search Cards" style="font-family:Arial, FontAwesome" />
      </b-nav-form>


      </b-collapse>
      <!-- Right aligned nav items -->
    <b-navbar-nav class="mx-2">

<!-- profile -->
        <div class="container d-flex justify-content-center d-none">
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
<!-- profile -->
          <b-collapse is-nav id="nav_collapse">
          <b-nav-item href="messageArea" class=""><fa :icon="fas.faComments"  :style="{ color: '' }" class="fa-lg m-3"/></b-nav-item>

          <b-nav-item-dropdown right>
            <!-- Using button-content slot -->
            <template slot="button-content">
              <em class=""><fa :icon="fas.faEllipsisV"  :style="{ color: '' }" class="fa-lg m-3 justify-content-center" /></em>
            </template>
            <b-dropdown-item href="settings">Settings</b-dropdown-item>
            <b-dropdown-item href="/">Signout</b-dropdown-item>
          </b-nav-item-dropdown>
          </b-collapse>
    </b-navbar-nav>
    


    </b-navbar>
  </div>
</template>

<script>
import { fas } from "@fortawesome/free-solid-svg-icons";
import { faGithub } from "@fortawesome/free-brands-svg-icons";
export default {
  data() {
    return {
      userName: "Iikai",
      userPower: "User"
    };
  },
  computed: {
    fas() {
      return fas;
    },
    faGithub() {
      return faGithub;
    }
  }
};
</script>


<style>
.header {
  padding: 0;
  padding-top: 0.1rem;
  background-color: #2a2e43 !important;
  width: 100%;
}

.logo-opus {
  height: 2.8rem;
  width: auto;
}

.img-profile {
  height: 3rem;
  width: auto;
  align-content: center;
  border-radius: 50%;
  margin-bottom: 5px;
}

/* Input */

.input-search{
    font-size: 16px;
    padding-right: 4rem;
    padding-top: 1.25rem;
    padding-bottom: 1.25rem;
    font-family:sans-serif;
    font-variant-position: normal;
    display: inline-block;
    background-color: #5d6177;
    border-style: none;
    border-radius: 0;
    vertical-align: top;
}

/* .input-search:forcus, .input-search:active{
  background-color: #5d6177;
} */

/* Input */


/* Icons */
.dropdown-toggle::after {
    display:none;
}


/* Icons */


/* Profile details */

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

/* Profile details */


.navbar-dark .navbar-toggler {
    border-width: 0;
}



</style>
