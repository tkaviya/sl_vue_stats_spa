<template>
    <div class="vue-tempalte">
        <form>
            <h3>Sign In</h3>

            <div class="form-group">
                <label>
                    Email address<br/><br/>
                    <input type="email" class="form-control form-control-lg" v-model="login_email" />
                </label>
            </div>
            <br/>
            <div class="form-group">
                <label>
                    Password<br/><br/>
                    <input type="password" class="form-control form-control-lg" v-model="login_password" /><br/>
                </label>
            </div>

            <button type="submit" class="btn btn-dark btn-lg btn-block">Sign In</button>

            <p class="forgot-password text-right mt-2 mb-4">
                <router-link to="/forgot-password">Forgot password ?</router-link>
            </p>

<!--            <div class="social-icons">-->
<!--                <ul>-->
<!--                    <li><a href="#"><i class="fa fa-google"></i></a></li>-->
<!--                    <li><a href="#"><i class="fa fa-facebook"></i></a></li>-->
<!--                    <li><a href="#"><i class="fa fa-twitter"></i></a></li>-->
<!--                </ul>-->
<!--            </div>-->

        </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                login_email: '',
                login_password: '',
            }
        }
    }
</script>
