<template>
    <div class="vue-tempalte">
        <form>
            <h3>Sign Up</h3>

            <div class="form-group">
                <label>
                    Full Name<br/><br/>
                    <input type="text" class="form-control form-control-lg"/>
                </label>
            </div>
            <br/>

            <div class="form-group">
                <label>
                    Email address<br/><br/>
                    <input type="email" class="form-control form-control-lg" />
                </label>
            </div>
            <br/>

            <div class="form-group">
                <label>
                    Password<br/><br/>
                    <input type="password" class="form-control form-control-lg" />
                </label>
            </div>
            <br/>

            <button type="submit" class="btn btn-dark btn-lg btn-block">Sign Up</button>

            <p class="forgot-password text-right">
                Already registered
                <router-link :to="{name: 'login'}">sign in?</router-link>
            </p>
        </form>
    </div>
</template>

<script>
    export default {
        data() {
            return {}
        }
    }
</script>
