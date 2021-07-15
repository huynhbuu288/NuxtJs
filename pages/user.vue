<template>
    <div>
        <ul>
            <li><nuxt-link  to="/user">user pages</nuxt-link></li>
            <li><nuxt-link  to="/user/20" tag="button">user details</nuxt-link></li>
            <li><nuxt-link  to="/user/settings">user settings</nuxt-link></li>
        </ul>
        <h1>users pages users.vue</h1>
        <p>lê huỳnh bửu </p>
        <nuxt-child />
    </div>
</template>


<script>
    export default {
        layout(context) {
            let userAgent = '';
            if(context.req) {
                userAgent = context.req.headers['user-agent']
            }else {
                userAgent = navigator.userAgent
            }
            if(/mobie/i.test(userAgent)) {
                return 'mobie';
            }
            return 'admin';
        }
  
    } 
</script>