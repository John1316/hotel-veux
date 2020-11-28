<template>
    <div id="signupForm" class="signup">
        <section class="login">
            <div class="bg-white login__card rounded shadow-7 p-6">
                <nav class="mt-8 row no-gutters justify-content-center">
                    <div class="nav nav-tabs" id="nav-tab" role="tablist">
                        <a class="nav-link active fs-20" id="nav-signin-tab" data-toggle="tab" href="#signinTab" role="tab" aria-controls="nav-home" aria-selected="true">Sign in</a>
                        <a class="nav-link fs-20" id="nav-signup-tab" data-toggle="tab" href="#signupTab" role="tab" aria-controls="nav-profile" aria-selected="false">Sign up</a>
                    </div>
                </nav>
                <div class="tab-content" id="nav-tabContent">
                    <!-- start Sign in -->
                    <div class="tab-pane fade show active row no-gutters align-items-center" id="signinTab" role="tabpanel" aria-labelledby="nav-signin-tab">
                        <h1 class="my-5 font-weight-bold">Sign in to your account</h1>
                        <h5 class="text-secondry">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt</h5>
                        
                        <form method="POST" action="" class="form-login" v-on:submit.prevent="submit">
                            <div class="row">
                                <div class="col-lg-8 col-12">
                                    <div class="form-group">
                                        <label for="email" class="font-weight-bold">Email address</label>
                                        <input type="email" v-model.trim="$v.email.$model" :class="{'is-invalid': validationStatus($v.email)}"  class="form-control border-secondry-1" name="email" placeholder="company@company.com">
                                        <div v-if="!$v.email.required" class="invalid-feedback">Provide a valid Email.</div>
                                    </div>
                                </div>
                                <div class="col-lg-8 col-12">
                                    <div class="form-group">
                                        <label for="password" class="font-weight-bold">Password</label>
                                        <div class="input-group border-secondry-1">
                                            <input type="password"  :class="{'is-invalid': validationStatus($v.password)}" v-model.trim="$v.password.$model" class="form-control" placeholder="8-20 Characters">
                                            <div class="input-group-append">
                                                <span class="input-group-text"><i class="fa fa-eye"></i></span>
                                            </div>
                                        </div>
                                        <div v-if="!$v.password.required" class="invalid-feedback">Provide a valid Password.</div>
                                    </div>
                                </div>
                            </div>
                            
                            
                            
                            <div class="form-group">
                                <div class="row no-gutters justify-content-start">
                                    <button class="btn btn-dark text-main btn-primary mr-4" type="submit">Sign in</button>
                                    <p class="text-center text-muted small-2 mb-0 font-weight-bold">Don't have an account? <a href="/signup#signupTab" class="text-main">Sign up here</a></p>                                
                                </div>
                            </div>
                        </form>
                    </div>
                    <!-- End Sign in -->
                    <!-- Start sign up -->
                    <div class="tab-pane fade" id="signupTab" role="tabpanel" aria-labelledby="nav-signup-tab">
                        <h1 class="my-5 font-weight-bold">Sign up account</h1>
                        <h5 class="text-secondry">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt</h5>
                        
                        <form method="POST" action="" class="form-login" v-on:submit.prevent="submit">
                            <div class="row">
                                <div class="col-lg-8 col-12">
                                    <div class="form-group">
                                        <label for="email" class="font-weight-bold">Email address</label>
                                        <input type="email" v-model.trim="$v.email.$model" :class="{'is-invalid': validationStatus($v.email)}"  class="form-control border-secondry-1" name="email" placeholder="company@company.com">
                                        <div v-if="!$v.email.required" class="invalid-feedback">Provide a valid Email.</div>
                                    </div>
                                </div>
                                <div class="col-lg-8 col-12">
                                    <div class="form-group">
                                        <label for="password" class="font-weight-bold">Password</label>
                                        <div class="input-group border-secondry-1">
                                            <input type="password"  :class="{'is-invalid': validationStatus($v.password)}" v-model.trim="$v.password.$model" class="form-control" placeholder="8-20 Characters">
                                            <div class="input-group-append">
                                                <span class="input-group-text"><i class="fa fa-eye"></i></span>
                                            </div>
                                        </div>
                                        <div v-if="!$v.password.required" class="invalid-feedback">Provide a valid Password.</div>
                                        
                                    </div>
                                </div>
                                <div class="col-lg-8 col-12">
                                    <div class="form-group">
                                        <label for="confirmPassword" class="font-weight-bold">Confirm Password</label>
                                        <div class="input-group border-secondry-1">
                                            <input type="password" data-toggle="tooltip" data-placement="top" title="Tooltip on top"  :class="{'is-invalid': validationStatus($v.confirmPassword)}" v-model.trim="$v.confirmPassword.$model" class="form-control" placeholder="Confirm your password">
                                            <div class="input-group-append">
                                                <span class="input-group-text"><i class="fa fa-eye"></i></span>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            
                            
                            
                            
                            <div class="form-group">
                                <div class="row no-gutters justify-content-start">
                                    <button class="btn btn-dark text-main btn-primary mr-4" type="submit">Sign up</button>
                                    <p class="text-center text-muted small-2 mb-0 font-weight-bold">Already have an account? <a href="user-login.html" class="text-main">Login here</a></p>                                
                                </div>
                            </div>
                        </form>
                    </div>
                    <!-- Start sign up -->
                </div>
                
            </div>
        </section>
    </div>
</template>

<script>

import { required , minLength , maxLength} from 'vuelidate/lib/validators'
export default {
    name: 'signupForm',
    data:function(){
        return{
            email: '',
            password:'',
            confirmPassword:''

        }
    },
    validations: {
        email:{required},
        password:{required , minLength:minLength(6) , maxLength: maxLength(20)},
        confirmPassword:{required}
    },
    methods: {
        validationStatus:function(validation){
            return typeof validation != "undefined" ? validation.$error : false ; 
        },
        submit: function(){
            this.$v.$touch();
            if(this.$v.$pendding || this.$v.$error) return;
            alert("data submited")
        }
    },
    
}
</script>