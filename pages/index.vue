<template>
    <section>
        <div class="container-fluid">
            <div class="row no-gutters">
                <div class="col-lg-8 col-md-5 col-sm-12 d-none d-md-block bg-left">
                    <div class="row justify-content-md-center txt-copyright">
                        <p class="text-muted copyright"><strong>Copyright © 2018 Arimac Lanka. All rights reserved.</strong></p>
                    </div>
                </div>
                <div class="col-lg-4 col-md-7 col-sm-12 bg-right ">
                    <div class="row justify-content-md-center">
                    <div class="col-lg-9 col-md-8 col-sm-7 col-xs-6 box-container">
                        <div class="row justify-content-md-center my-5">
                            <b-img src="/logo-opus.jpg" fluid alt="OPUS" />
                        </div>
                        <div class="row justify-content-md-center my-4">
                            <div class="form-group">
                                <ReusableInput active type="text" v-model="login.email" placeholder="email" @inputEvent="inputEvent"></ReusableInput>
                                <ReusableInput type="password" v-model="login.password" placeholder="password" @inputEvent="inputEvent"></ReusableInput>
                            </div>
                        </div>
                        <div class="row justify-content-md-center">
                            <Reusable-button label="Login" class="btn-login" :onClick="onLogin" v-bind:style="{'background-color':btnBgColor, color:btnColor}"></Reusable-button>
                        </div>
                        <div class="d-flex justify-content-center align-items-center d-block d-md-none fixed-bottom">
                          <p class="text-muted copyright mx-3">Copyright © 2018 Arimac Lanka. All rights reserved.</p>
                        </div>
                    </div>
                    </div>
                </div>
            </div>
        </div>
    </section> 
</template>

<script>
import ReusableButton from "~/components/ReusableButton.vue";
import ReusableInput from "~/components/ReusableInput.vue";

export default {
  data() {
    return {
      btnBgColor: "#e74132",
      btnColor: "#fff",
      login:{
        email:'',
        password:''  
      }
    };
  },
  components: {
    ReusableButton,
    ReusableInput
  },
  methods: {

      onLogin: function() {
      console.log("LogIn Clicked");
      // this.$router.push("homeUser");
      const loginData ={
        email: this.login.email,
        password: this.login.password
      }
      console.log(loginData)
      this.$axios.post('http://opus-api.devops.arimac.xyz/webapi/auth/login', loginData)
                .then(response => {
                    console.log(response.data)
                    console.log(response.status)
                    console.log(response.headers)
                    console.log(response.message)
                    if(response.status===200){
                      this.$router.push("homeUser");
                    }
                })
  .catch(function (error) {
    if (error.response) {
      // The request was made and the server responded with a status code
      // that falls out of the range of 2xx
      console.log(error.response.data);
      console.log(error.response.status);
      console.log(error.response.headers);
    } else if (error.request) {
      // The request was made but no response was received
      // `error.request` is an instance of XMLHttpRequest in the browser and an instance of
      // http.ClientRequest in node.js
      console.log(error.request);
    } else {
      // Something happened in setting up the request that triggered an Error
      console.log('Error', error.message);
    }
    console.log(error.config);
  });
    },
    inputEvent(e) {
            // console.log(e);
    }
  }
};
</script>


<style>
* {
  /* outline: 0; */
  font-family: Montserrat, sans-serif;
}

html,body
{
    width: 100%;
    height: 100%;
    margin: 0px;
    padding: 0px;
    /* overflow-x: hidden;  */
}

body {
  /* overflow-y: hidden; */
}

.bg-left, .bg-right{
  height: 100vh;
}

.container-fluid {
  padding: 0;
}

.bg-left {
    background: url("/img-login.jpg");
    background-size: cover;
}

.txt-copyright{
  box-sizing: border-box;
  margin: 95vh 5vh 0 5vh;
}

.copyright{
    font-size: 0.8em;
    text-align: center;
    overflow: hidden;
}

.bg-right {
  background-color: #e6ebf1;
}

.box-container {
  margin: 50px;
  justify-content: center;
}


.form-group{
  width: 100%;
}


@media (max-width: 768px) {
  * {
    justify-content: center;
  }

}

@media (max-width: 480px) {
  * {
    justify-content: center;
  }


}
</style>
