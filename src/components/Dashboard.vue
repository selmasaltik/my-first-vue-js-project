<template>
    <div>
        <div v-if="show" class="userBar">
            Hello {{ userName }}
        </div>
        <div v-else-if="!show" class="guestBar">
            Welcome to our website. Please register or login!
        </div>
        <button v-on:click="showData">Login/Logout</button>
 </div>
</template>

<script>
export default {
    name : 'Dashboard',
    data() {
        return {
           userName : 'John SMITH',
           show : true,
            };
    },
    methods : {
        showData : function() {
            this.show = !this.show;
            }
        }
};
</script>

<style>

</style>