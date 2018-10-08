<template>
    <div>
    <b-card no-body
            style="max-width: 26rem;"
            >
        <b-card-body>
<div class="row">
  <div class="column11">
    
    <p><fa :icon="fas.faExclamationCircle"  :style="{ color: '' }" class="fa-size" /></p>
  </div>
  <div class="column12 text-right">
      <h6>Task default‑ Lorem ipsum dolor sit amet, consectetur adipiscing elit,</h6>    
       <p class="card-text">Project default Lorem ipsum dolor sit amet</p>
  </div>

</div>
        </b-card-body>
        <b-card-footer>
<div class="row">
  <div class="column">
    
    <p><fa :icon="fas.faExclamationTriangle"  :style="{ color: '' }" class="fa-size" />  2 days left</p>
  </div>
  <div class="column text-right">
    
    <p> June 15th 2016</p>
  </div>

</div>
        
            
        </b-card-footer>
    </b-card>

    </div>
</template>

<script>
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

<style>
.card {
    position: relative;
    display: -ms-flexbox;
    display: -webkit-box;
    display: flex;
    -ms-flex-direction: column;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-direction: column;
    min-width: 0;
    word-wrap: break-word;
    background-color: #fff;
    background-clip: border-box;
    border-radius: 0.25rem;
    margin-bottom: 1.3rem;
    margin-top: 1.3rem;
}
/* 34c0dd - tasks blue */

.card-footer {
    padding: 0.75rem 1.25rem;
    background-color: #39c379;
    border-top: 1px solid rgba(0, 0, 0, 0.125);
}

.center{
    display: flex;
    align-items: center;
    justify-content: center;
}

.txt-left {
    text-align: left !important;
}

.txt-right {
    text-align: left !important;
}

.col2{
    column-gap: 40px;
    column-count: 3;
}


/*Column Layoutl*/

* {
    box-sizing: border-box;
}

/* Create three equal columns that floats next to each other */
.column11 {
    float: left;
    width: 15%;
    padding: 0;
    height: 4rem; /* Should be removed. Only for demonstration */
}
.column12 {
    float: left;
    width: 85%;
    padding: 0;
    height: 4rem; /* Should be removed. Only for demonstration */
}
.column {
    float: left;
    width: 50%;
    padding: 0;
    height: 1rem; /* Should be removed. Only for demonstration */
}

/* Clear floats after the columns */
.row:after {
    content: "";
    display: table;
    clear: both;
}

/*Column Layoutl*/

/* .fa-size{
      height: 1.6rem;
      width: auto; 
} */

</style>
