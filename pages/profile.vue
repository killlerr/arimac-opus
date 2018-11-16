<template>
    <div class="bg-opus">
        <Header></Header>
        <div class="container">
            <div class="row profile-content py-5">
                <div class="col-md-6">
                    <b-card class="my-3">
                        <div class="p-4">
                            <h5>Profile</h5>
                            <div class="profile-hl"></div>
                        </div>
                        <div class="center-justify-everything">
                            <img src="img-profile-picture.jpeg" class="img-profile" alt="Cinque Terre">
                        </div>
                    </b-card>
                </div>
                <div class="col-md-6">
                    <b-card class="my-3">
                        <div class="p-4">
                            <h5>Deatils</h5>
                            <div class="profile-hl"></div>
                        </div>
                        <div class="px-4">
                            <!-- <label>Name:</label> -->
                            <ReusableInput v-model="profile.name" placeholder="Enter your name" class="profile-input"></ReusableInput>
                            <!-- <label>Contact Number:</label> -->
                            <ReusableInput v-model="profile.contactNumber" placeholder="Your contact Number" class="profile-input"></ReusableInput>
                            <div class="pt-4">
                                <ReusableButton label="Save" @click="onSave"></ReusableButton>
                            </div>
                        </div>
                    </b-card>
                </div>
            </div>                
        </div> 
    </div>
</template>

<script>
import ReusableInput from '~/components/ReusableInput.vue'
import ReusableButton from '~/components/ReusableButton.vue'
import Header from '~/components/Header.vue'
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
        ReusableInput,
        ReusableButton,
        Header
    },
    methods:{
        onSave(){
            console.log("Save Clicked")
        }
    }
}
</script>

<style>

.img-profile {
  height: 16rem;
  width: 16rem;
  align-content: center;
  border-radius: 50%;
  margin-bottom: 5px;
  display: block;
}

.bg-opus{
    background-color: #e6ebf1;
    height: 100vh; 
}

.profile-input input{
    background-color: #e8e8e8;
}

.center-justify-everything{
    display: flex;
    justify-content: center;
    align-content: center;
}

.profile-hl{
    border-bottom: 0.1rem solid #2a2e43;
    width: 100%;
}
</style>
