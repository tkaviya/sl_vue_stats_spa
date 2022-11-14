<template>
    <div class="vue-tempalte">
        <form>
            <h3>Sign In</h3>

            <div class="form-group">
                <label>
                    Email address<br/><br/>
                    <input type="text" class="form-control form-control-lg" v-model="login_email" />
                </label>
            </div>
            <br/>
            <div class="form-group">
                <label>
                    Password<br/><br/>
                    <input type="password" class="form-control form-control-lg" v-model="login_password" /><br/>
                </label>
            </div>

            <button v-on:click="doLogin" class="btn btn-dark btn-lg btn-block">Sign In</button>

            <br/>
            <span class="forgot-password" style="float: left">
                <router-link to="/">Register</router-link>
            </span>
            <span class="forgot-password text-right" style="float: right">
                <router-link to="/forgot-password">Forgot password?</router-link>
            </span>

        </form>
    </div>
</template>

<script>
    import axios from 'axios'
    export default {
        name: "Login",
        data() {
            return {
                login_email: '',
                login_password: '',
            }
        },
        methods: {
            async doLogin() {
                let result = await axios.post(
                    'http://localhost:8080/api/auth/login',
                    `{ "username": "${this.login_email}", "password": "${this.login_password}" }`,
                    { headers: { 'Content-Type': 'application/json' } }
                )
                console.warn(result);
            }
        }
    }
</script>
