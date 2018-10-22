<template>
  <p>test</p>
</template>
<template>
    <div>
        <div class="container-fluid py-3">
            <div class="row">
                <div class="col-md-7">
                    <div>
                        <b-card>
                            <div class="row">
                                <div class="col-12">
                                  <div class="p-3">
                                  <blockquote class="blockquote text-left">
                                    <p class="mb-0">What happen Today Attendance</p>
                                    <footer class="blockquote-footer">Lorem ipsum dolor sit amet, consectetur</footer>
                                  </blockquote>
                                  </div>
                                </div>
                            </div>
                            <div class="row">
                                <div class="col-md-3">
                                    <div class="pb-1 pl-3 pr-3"> 
                                        <b-dropdown id="ddown1" text="Today I'm" class="dropdown-top">

                                        </b-dropdown>
                                    </div>
                                </div>
                                <div class="col-md-4">
                                    <div class="p-3">
                                        <b-form-select id="exampleInput3"
                                        :options="attendenceCatagory"
                                        required
                                        v-model="form.attendenceCatagory"
                                        class="attendence-slect">
                                        </b-form-select>
                                    </div>
                                </div>
                                <div class="col-md-4">
                                    <div class="p-3">
                                        <Reusable-button label="Set" class="btn-login" :onClick="doSomething" v-bind:style="{'background-color':btnBgColor, color:btnColor}"></Reusable-button>
                                    </div>
                                </div>
                            </div>
                        </b-card>                     
                    </div>
                    <div class="pt-5">
                        <b-card>
                            <div class="p-3">
                                <blockquote class="blockquote text-left">
                                    <p class="mb-0">Urgent message</p>
                                    <footer class="blockquote-footer">Lorem ipsum dolor sit amet, consectetur</footer>
                                </blockquote>                              
                            </div>
                            <div class="p-3">
                                <div class="form-group">
                                    <textarea class="type-here form-control rounded-0" id="exampleFormControlTextarea1" rows="10" placeholder="Type here"></textarea>
                                </div>
                            </div>
                        </b-card>
                    </div>
                </div>
                <div class="col-md-5">

                </div>
            </div>
        </div>
    </div>
</template>


<script>
import ReusableButton from "~/components/ReusableButton.vue";

export default {
    data() {
        return {
            btnBgColor: "#e74132",
            btnColor: "#fff",
            form:{
                attendenceCatagory: null
            },
            attendenceCatagory: [
                { text: 'Select an attendence catagory', value: null },
                'Present', 'Absent', 'Working from home'
            ],
      show: true
        };
    },
    components:{
        ReusableButton
    },
    methods: {
        doSomething: function() {
            console.log("LogIn Clicked");
            this.$router.push("homeUser");
        }
    }
}
</script>


<style>

/* .drop-middle btn-group > .btn:first-child {
    width: 100%;
} */

.dropdown-top, .btn-group > .btn:first-child {
    width: 100%;
    padding-top: 12px;
    padding-bottom: 12px;
    margin: 2px;
    border-radius: 0;
}

.attendence-slect, .custom-select{
    height: calc(2.25rem + 16px);
    border-radius: 0;
}

.btn-login{
    padding: 17px;
}

.type-here{
    background-color: #ecedf3e0
 
}
</style>
