<template>
<div>
    <h1>Users</h1>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Saepe quos sint ipsum eius nam deleniti, expedita illo, quibusdam velit reiciendis sapiente sed molestiae esse porro quod nemo blanditiis id asperiores.</p>
    <p>Name: {{ firstName }}</p>
    <p>Surname: {{ lastName }}</p>
    <p>Full Name: {{ myFullName() }}</p>

    <input type="text" v-model="firstName">
    <input type="text" v-model="lastName">
    <p> {{fullName}} </p>
    <hr>

</div>
</template>

<script>
export default {
    name : 'UserList',
    data() {
        return {
       firstName : 'Jane',
       lastName : 'DOE',
       location : 'Turkey' 
       };
    },
    computed : {
        fullName : function() {
            return this.firstName + " " + this.lastName;
            }
        },
    methods : {
        myFullName : function () {
            return "My name is " + this.firstName + " " + this.lastName;
            }
        }
};
</script>

<style>

</style>