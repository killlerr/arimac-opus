<template>
<div class="bg-wrap">
    <div class="row">
        <div class="col-7 img-login">

        </div>
        <div class="col-5">
            <div class="login-box">
                <b-img src="/logo-opus.jpg" class="logo" fluid alt="Responsive image" />
                    
                    <div class="row row-gap">
                        <div class="form-group">
                            <input type="text" class="form-control" id="usrName" placeholder="email">
                        </div>
                    </div>
                    <div class="row row-gap">
                        <div class="form-group">
                            <input type="password" class="form-control" id="usrPassword" placeholder="password">
                        </div>
                    
                    </div>
                    
                    <div class="row row-gap">
                        <Base-button label="Login" :onClick="doSomething"></Base-button>
                    </div>
                    
            </div>
        </div>

    </div>    
</div>

</template>

<script>
import BaseButton from '~/components/BaseButton.vue'
import BaseInputText from '~/components/BaseInputText.vue'
import BaseOpusLogo from '~/components/BaseOpusLogo.vue'

export default {
    data() {
        return{
            userId:''
        }
    },
    components: {
        BaseButton,
        BaseInputText,
        BaseOpusLogo
    },
    methods: {
        doSomething: function () {
            // <nuxt-link to="appTasks"></nuxt-link>
            this.$router.push('/users/' + this.userId)
        }
    }
}
</script>


<style>
* {
    padding: 0;
    margin: 0 ;
    box-sizing: inherit;
    /*change the box-modle to where borders and paddings are no longer added to total width or height*/
}
html{
    font-size: 62.5%;
}

body{
    font-family: "Lato", sans-serif;
    background-color: #ffffff;
    line-height: 1.7;
    box-sizing: border-box;
    /*change the box-modle to where borders and paddings are no longer added to total width or height*/
    margin-left: 12rem;
    margin-right: 12rem;
    

}

.bg-wrap{
    background-color: #e6ebf1 ;
}

.img-login {
    height: 100vh;
    background-size: cover;
    /*What everth width of the image it fits into the view-port*/
    background-image: url(/img-login.jpg);
    background-position: top;
}

.login-box{
    height: 100vh;
    background-size: cover;
    padding-left: 10rem;
    padding-right: 10rem;
    padding-top: 20rem;
    text-align: center;
}

.form-group{
    width: 100%;
}

.form-control{

    width: 100%;
    font-size: 11px;
    padding: 2.7rem;
    font-family:sans-serif;
    letter-spacing: 1px;
    display: inline-block;
    text-transform: uppercase;
    color: #9f9f9f;
    border-style: none;
    border-radius: 0;

    /* &:not(:placeholder-shown)
      + span
        color #5A667F;
        transform: translateY(-26px) scale(.75); */
}

.form-control:visited{
    color: #5A667F;
    transform: translateY(-26px) scale(.75);
    border-left: 6px solid red;
}

.row-gap{
    padding-top: 1rem;
}

.logo{
    margin-bottom: 3rem;
}


</style>
