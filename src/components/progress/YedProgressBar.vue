<template>
    <div class="yedprogress" >
        <div class="yedprogressbar" :class="progressStripeMode===false?progressColor:progressStripe" :style="{width:percent+'%'}">
        </div>
            <div class="yedprogresstext" :style="{color:progressTextColor}"><em> %{{percent}}</em></div>

    </div>
</template>

<script>
    import "./yedprogressbar.css"
    export default {
        name: "YedProgressBar",
        props:{
            progressColor:{
                type:String,
                required: false,
                default:"colorBlue",
                validator:function(value){
                    return ['colorRed', 'colorOrange', 'colorYellow','colorGreen','colorPurple','colorPink','colorBlue'].indexOf(value) !== -1
                }
            },
            progressStripeMode:{
                type:Boolean,
                required:false
            },
            progressStripe:{
                type:String,
                required:false,
                default:"stripeBlue",
                validator:function(value){
                    return ['stripeGray', 'stripeGreen', 'stripeYellow','stripePurple','stripePink','stripeOrange','stripeRed','stripeBlue'].indexOf(value) !== -1
                }
            },
            progressTextColor:{
                type:String,
                required:false,
                default: "#fff"
            },
            percent:{
                type:Number,
                required:true
            }
        }
    }

</script>

<style scoped>



</style>
