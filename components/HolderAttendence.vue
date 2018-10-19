<template>
    <div>
        <div class="col-7">
            <div class="row">
                <div class="top-box card-border">
<blockquote class="blockquote text-right">
  <p class="mb-0">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
  <footer class="blockquote-footer">Someone famous in <cite title="Source Title">Source Title</cite></footer>
</blockquote>

<div class="row">
<div class="col-4">

</div>

  <div class="col-4">
    <b-form-select v-model="selected" :options="options" class="mb-3 r-h">
      <template slot="first">
        <!-- this slot appears above the options from 'options' prop -->
        <option :value="null" disabled>-- Please select an option --</option>
      </template>
      <!-- these options will appear after the ones from 'options' prop -->
      <option value="C">Option C</option>
      <option value="D">Option D</option>
    </b-form-select>
    <!-- <div>Selected: <strong>{{ selected }}</strong></div> -->
  </div>

<div class="col-4">
<Reusable-button label="set" :onClick="doSomething" class=" r-h text-center"></Reusable-button>
</div>
                </div>

</div>

                <div class="bottom-box card-border">
<blockquote class="blockquote text-right">
  <p class="mb-0">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
  <footer class="blockquote-footer">Someone famous in <cite title="Source Title">Source Title</cite></footer>
</blockquote> 

  <div class="w-100 mx-6">
    <b-form-textarea id="textarea1"
                     v-model="text"
                     placeholder="Type here"
                     :rows="4"
                     :max-rows="6">
    </b-form-textarea>
    <pre class="mt-3">{{ text }}</pre>
  </div>
                </div>
            </div>
        </div>
        <div class="col-5">

        </div>
    </div>
</template>

<script>
import ReusableButton from '../components/ReusableButton.vue';
import Vue from 'vue';
import iView from 'iview';

Vue.use(iView);
import 'iview/dist/styles/iview.css';

export default {


  data () {
    return {
      text: '',
      selected: null,
      options: [
        { value: 'A', text: 'Option A (from options prop)' },
        { value: 'B', text: 'Option B (from options prop)' }
      ]
    }
  },
  components:{
      ReusableButton
  },
  methods: {
        doSomething: function () {
            // <nuxt-link to="appTasks"></nuxt-link>
            console.log("Clicked");
        }
    }  
}
</script>

<style scoped>

.card-border{
        box-shadow: 0 0.05rem 0.2rem 0 rgba(0, 0, 0, 0.2);
}

.top-box{
    height: 40%;
    width: 100%;
    margin: 2rem 2rem 2rem;
    padding: 1rem 2rem;
}

.bottom-box{
    height: 60%;
    width: 100%;
    margin: 2rem 2rem 2rem;
    padding: 1rem 2rem;
    justify-content: center;
}

.r-h{
    height: 3rem;
}

.text-center{
    /* Button text center */
  display: inline-flex;
  align-items: center; /* cross axis */
  justify-content: center; /* main axis */

  line-height: 1; /* reset */
  /* Button text center */
    
}
</style>
