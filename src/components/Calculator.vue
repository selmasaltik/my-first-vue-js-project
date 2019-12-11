<template>
    <div>
        <h2> {{ title }} </h2>
        <a v-bind:href="links" target="_blank">Google</a>
        <hr>
        Kilometer
        <input type="text" v-model="kilometers">
        <br><br>
        Meter
        <input type="text" v-model="meters">
        <hr>
         <input type="text" v-model="num1">
          <input type="text" v-model="num2">
        <button v-on:click="displayNumber">Click</button>
        <p>Numbers: {{num1}} + {{num2}} <br>RESULT: {{total }}<br></p>
        <hr>
 </div>
</template>

<script>
export default {
    name : 'Calculator',
    data() {
        return {
            title : 'Binding',
            links : 'https:www.google.com.tr',
            kilometers: 0,
            meters: 0,
            num1: 10,
            num2: 20,
            total : ''
            };
    },
    methods : {
        displayNumber : function() {
            return this.total = parseInt(this.num1) + parseInt(this.num2);
            }
        },
    watch : {
        kilometers : function(data) {
            this.kilometers = data;
            this.meters = data * 1000;
            },
        meters : function(data) {
            this.kilometers = data / 1000;
            this.meters = data;
            }
        }
};
</script>

<style>

</style>