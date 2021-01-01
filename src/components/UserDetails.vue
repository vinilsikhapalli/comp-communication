<template>
    <div class="component">
        <h3>You may view the User Details here</h3>
        <p>Many Details</p>
        <h1> the name is {{ changeNameInChild() }}</h1>
    </div>
</template>

<script>

export default{
    props:['passName'],

    methods:{
        changeNameInChild(){
            return this.passName;
        }
    }
}

</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
 