<template>
    <div id = "sidebar">
        <div v-if="auth.user !== null">
        <Sidebar></Sidebar>
            <transition>
                 <router-view></router-view>
            </transition>
        </div>
    <div v-else>
        <transition>
        <router-view></router-view>
        </transition>
    </div>
    </div>
</template>
<style scope>
</style>
<script>
import Sidebar from "router/frame/Sidebar.vue";
import AUTH from "services/auth"
export default {
    name: "sidebar",
    components: {
        Sidebar
    },
    data(){
        return {
            auth: AUTH,
        }
    }
    
}
</script>