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
                            <label for="task-name">Task Name</label>
                            <b-form-input type="text"
                            placeholder="Add task name here"
                            id="task-name"></b-form-input>
                        </div>
                        <div class="py-2">
                            <label for="task-name2">Project Name</label>
                            <b-form-input type="text"
                            placeholder="Add task name here"
                            id="task-name2"></b-form-input>
                        </div>
                        <div class="py-2">
                            <label for="task-name3">Due date</label>
                            <b-form-input type="text"
                            placeholder="Add task name here"
                            id="task-name3"></b-form-input>
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
export default {
    components:{
        ReusableButton
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
}

.p-0 .modal-body {
    padding: 0;
}

.btn-add-card{
    background-color: #e74132;
    color:#fff;   
}
</style>
