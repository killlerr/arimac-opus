<template>
    <div class="row">
      <div>
        <b-card class="card-front fit-content" @click="onAnswer">
            <div class="card-content">
        <div class="row card-header">
            <div class="col-3">
                <p><fa :icon="fas.faCommentAlt" v-bind:style="{color:bgColor}"/></p>
            </div>
            <div class="col-9 text-left">
                <div class="row">
                    <strong>{{taskName}}</strong>
                </div>
                <div class="row">
                    <small>{{projectName}}</small>  
                </div>                  
            </div>
        </div>
        <div class="row card-footer" v-bind:style="{'background-color':bgColor}">
            <div class="col-6 text-left">
                <fa :icon="fas.faExclamationTriangle" style="{color: #ffffff}" class="fa-size" />
                {{daysLeft}}           
            </div>
            <div class="col-6 text-right">
                {{dueDate}}
            </div>
        </div>
            </div>
        </b-card>
      </div>
    </div>



</template>

<script>
import { fas } from '@fortawesome/free-solid-svg-icons'
import { faGithub } from '@fortawesome/free-brands-svg-icons'


export default {
    data(){
        return{
        bgColor: '#ff5a4e',
        taskName: 'default‑ Lorem ,',
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
    padding: 0;
}

.card-front{
    position: relative;
    display: flex;
    box-sizing: border-box;
    align-items: center;
    justify-content: center;
    height: 9.99rem;
    max-height: 14rem;
    min-width: 0;
    width: 100%;
    border-radius: 0.25rem;
    box-shadow: 0 0.05rem 0.2rem 0 rgba(0, 0, 0, 0.2);
    word-wrap: break-word;
    margin: 1.3rem 0 1.3rem 0;
}

.card-header{
    color: #80818cfa;
    height: 6.66rem;
    width: 100%;
    min-width: 95%;

}

.card-footer{
    color: #ffffff;
    height: 3.33rem;
    width: 100%;
    min-width: 95%;
}



.card-content{
    
}

</style>
