<template>
    <div class="component">
        <h3>You may view the User Details here</h3>
        <p>Many Details</p>
        <h1> the name is {{ changeNameInChild() }}</h1>
        <p> age is from sibling {{ userAge }}</p>
    </div>
</template>

<script>
import { serviceBus } from '../main'
export default{
    
    props:{
        passName:{
            type:String,
            required:false,
            default:'i am the one from validation'
        },
        userAge:{
            type:Number
        }
        
        },

    methods:{
        changeNameInChild(){
            return this.passName;
        }
    },
    created(){
    serviceBus.$on('chnageAge',(data) => {
        this.userAge = data
    });
    }

}

</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
 