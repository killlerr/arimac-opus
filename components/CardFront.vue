<template>

      <div class="pb-2 pt-2">
        <b-card class="card-front fit-content" @click="onAnswer">
            <div class="card-content">
              <div class="row card-header no-gutters">
                <div class="col-2 text-right">
                  <div class="pr-3 pt-3">
                    <p><fa :icon="fas.faCommentAlt" v-bind:style="{color:bgColor}" class="fa-2x"/></p>
                  </div>
                </div>
              <div class="col-10 text-left">
                <div class="pl-3 pr-3 pb-3 pt-2">
                  <div class="row no-gutters task-name">
                    {{taskName}}
                  </div>
                  <div class="row no-gutters project-name">
                    {{projectName}} 
                  </div>                   
                </div>                  
              </div>
              </div>
              <div class="row card-footer no-gutters" v-bind:style="{'background-color':bgColor}">
                <div class="col-6 text-left">
                  <div class="d-flex fex-column">
                  <div class="pt-1 pr-2">
                  <fa :icon="fas.faExclamationTriangle" style="{color: #ffffff}" class="fa-lg" />
                  </div>

                  <div class="pl-2 days-left pt-1">{{daysLeft}}</div>
                  </div>
                </div>
                <div class="col-6 text-right due-date pt-2">
                  {{dueDate}}
                </div>
              </div>
            </div>
        </b-card>
      </div>




</template>

<script>
import { fas } from '@fortawesome/free-solid-svg-icons'
import { faGithub } from '@fortawesome/free-brands-svg-icons'


export default {
    data(){
        return{
        bgColor: '#ff5a4e',
        taskName: 'Task default‑ Lorem ipsum dolor sit amet, consectetur adipiscing elit,',
        projectName: 'default Lorem ipsum dolor sit amet',
        dueDate: 'June 15th 2016',
        daysLeft: '2 days left'
        }
    },
    methods:{
            onAnswer(){
            this.$emit('answered');
            }
    },

    computed: {
      fas () {
         return fas
      },
      faGithub () {
         return faGithub
      }
    }
}
</script>

<style scoped>

.card-body {
    width: 100%;
    height: 100%;

    padding: 0px;
}

.card-front{

    width: 100%;
    border-radius: 0.25rem;
    box-shadow: 0 0.05rem 0.2rem 0 rgba(0, 0, 0, 0.2);
    word-wrap: break-word;
}

.card-header{
    color: #80818cfa;
    height: 6.66rem;
}

.card-footer{
    color: #ffffff;
    height: 3.33rem;
}

/*Text styling*/

.task-name{
    /* font-weight: 600; */
    font-size: 0.938em;
    line-height: normal;

}

.project-name{
  font-weight: bold;
  margin-top: 1em;
  color: #b8b8bb;
  font-size: 0.688em;
}

.days-left{
  font-size: 1.125em;
}

.due-date{
  font-size: 10px;
  font-weight: lighter;
}

/*Text styling*/

</style>
