<template>
    <div class="bg-opus p-4">
        <b-card>
            <div class="container">
                <!-- <div class="row"> -->
                    <h4 class="profile-h">Profile</h4>
                <!-- </div> -->
                <div class="row profile-content">
                    <div class="col-md-6">
                            <img src="img-profile-picture.jpeg" class="img-circle img-profile" alt="Cinque Terre">
                    </div>
                    <div class="col-md-6">
                        <label>Name:</label>
                        <ReusableInput v-model="profile.name" placeholder="Enter your name"></ReusableInput>
                        <label>Contact Number:</label>
                        <ReusableInput v-model="profile.contactNumber" placeholder="Your contact Numberf"></ReusableInput>
                    </div>
                </div>
                
            </div>
        </b-card>   
    </div>
</template>

<script>
import ReusableInput from '~/components/ReusableInput.vue'
export default {
    data(){
        return{
            profile:{
                name:"",
                contactNumber:""
            }
        }
    },
    components:{
        ReusableInput
    }
}
</script>

<style>

.img-profile {
  height: 16rem;
  width: auto;
  align-content: center;
  border-radius: 50%;
  margin-bottom: 5px;
}

.bg-opus{
      background-color: #e6ebf1;
}
</style>
