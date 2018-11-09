<template>
  <div>
    <ReusableButton v-b-modal.modalPrevent :onClick="doSomething" label="Add new task card" class="btn-add-new-task"></ReusableButton>
    <!-- Main UI -->
    <!-- <div class="mt-3 mb-3">
        <CardFlip
            v-for="(item,index) in items"
            v-bind:item="item"
            v-bind:index="index"
            v-bind:key="item.id"
        ></CardFlip>
    </div> -->
    <!-- Modal Component -->
    <b-modal id="modalPrevent" size="lg" centered :hide-header="true" :hide-footer='true' class="p-0">
        <div class="container-fluid">
            <div class="row no-gutters">
                <div class="col-md-6">
                    <div class="text-center py-4">
                        <h5>TASK CARD ADD</h5>
                    </div>
                    <div class="p-4">
                    <form @submit.stop.prevent="handleSubmit">
                        <div class="py-2">
                            <label for="task-name"><small>Name</small></label>
                            <b-form-input type="text"
                            placeholder="Add task name here"
                            id="task-name"></b-form-input>
                        </div>
                        <div class="py-2">
                            <!-- input-select -->
                            <label for="task-name2"><small>Project Name</small></label>
                            <!-- <b-form-input type="text"
                            placeholder="Add task name here"
                            id="task-name2"></b-form-input> -->
                            <cool-select

                            />
                        </div>
                        <div class="py-2">
                            <label for="task-name3"><small>Due date</small></label><br>
                            <!-- <b-form-input type="text"
                            placeholder="Add task name here"
                            id="task-name3"></b-form-input> --><date-picker v-model="time1" :first-day-of-week="1" lang="en"></date-picker>
                        </div>   
                    </form>
                        <div class="pt-4 pb-5">
                            <ReusableButton :onClick="addCard" label="Add card" class="btn-login btn-add-card"></ReusableButton>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 img-login">

                </div>
            </div>
        </div>
    </b-modal>
  </div>
</template>

<script>
import ReusableButton from '~/components/ReusableButton.vue'
import DatePicker from 'vue2-datepicker'
import { CoolSelect } from 'vue-cool-select'

export default {   
    data() {
        return {
        time1: '',
        time2: '',
        time3: '',
        shortcuts: [
            {
            text: 'Today',
            onClick: () => {
                this.time3 = [ new Date(), new Date() ]
            }
            }
        ],
        timePickerOptions:{
            start: '00:00',
            step: '00:30',
            end: '23:30'
        }
        }
    },
    components:{
        ReusableButton,
        DatePicker,
        CoolSelect
    },
    methods: {
        doSomething: function() {
        console.log("Add new task card Clicked");
        },   
        addCard: function() {
        console.log("Card added");
        },   
    }
}
</script>

<style>

.btn-add-new-task{
    border-radius: 0.25rem;
    box-shadow: 0 0.05rem 0.2rem 0 rgba(0, 0, 0, 0.2);
    width: 100%;
    background-color: #ffffff;
    color:#80818cfa;
}

.img-login {
    background-size: cover;
    /*What everth width of the image it fits into the view-port*/
    background-image: url(/img-login.jpg);
    border: 0;
    border-radius: 0 1rem 1rem 0;
}

.p-0 .modal-body {
    padding: 0;
    border-radius: 1rem;
}

.p-0 .modal-content {
    border-radius: 1rem;
}



.btn-add-card{
    background-color: #e74132;
    color:#fff;   
}


/* Date-picker */

.mx-input{
    width: 100%;
}

.mx-datepicker{
    width: 100%;
}

/* Date-picker */
</style>
