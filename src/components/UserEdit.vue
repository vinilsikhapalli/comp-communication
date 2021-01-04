<template>
    <div class="component">
        <h3>You may edit the User here</h3>
        <p>Edit me!</p>
        <p>age is {{ age }}</p>
        <button @click="changeAge" >changeAge</button>
    </div>
</template>

<script>

import { serviceBus } from '../main'

export default {

props:['age'],

methods:{
    changeAge(){
        serviceBus.$emit('chnageAge' , 45);
    }
}

}

</script>

<style scoped>
    div {
        background-color: lightgreen;
    }
</style>
