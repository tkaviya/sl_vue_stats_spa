<template>
    <div class="vue-tempalte">
        <form>
            <h3>Forgot Password</h3>

            <div class="form-group">
                <label>
                    Email address<br/><br/>
                    <input type="email" class="form-control form-control-lg" />
                </label>
            </div>
            <br/>

            <button type="submit" class="btn btn-dark btn-lg btn-block">Reset password</button>

            <p class="forgot-password text-right mt-2 mb-4">
                <router-link to="/login">Sign In</router-link> or
                <router-link to="/">Sign Up</router-link>
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
