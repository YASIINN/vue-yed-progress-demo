<template>
    <div id="app">
        <vue-yed-progressbar :percent="70"/>
        <br/>
        <vue-yed-progressbar :percent="80" progressColor="colorPink"/>
        <br/>
        <vue-yed-progressbar :percent="40" progressColor="colorPurple" progressTextColor="black"/>
        <br/>
        <vue-yed-progressbar :percent="79" progressStripe="stripePurple" :progressStripeMode="true"/>
        <br/>
        <vue-yed-progressbar :percent="68" progressStripe="stripeGreen" :progressStripeMode="true"/>



    </div>
</template>
<script>
    import VueYedProgressbar from "vue-yed-progressbar"
    export default {
        name: 'App',
        components: {
            VueYedProgressbar
        },
    }
</script>
<style>
    body{
        padding: 40px;
    }
</style>


