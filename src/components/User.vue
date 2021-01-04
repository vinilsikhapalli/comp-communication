<template>
    <div class="component">
        <h1>The User Component</h1>
        <p>I'm an awesome User!</p>
        <p>user age {{ age }} </p>
        <button v-on:click="changeName"> click here to chnage name </button>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-6">
                <app-user-detail :passName="passName" :userAge="age"></app-user-detail>
            </div> 
            <div class="col-xs-12 col-sm-6">
                <app-user-edit :age = "age"></app-user-edit>
            </div>
        </div>
    </div>
</template>

<script>
    import UserDetail from './UserDetails.vue';
    import UserEdit from './UserEdit.vue';

    export default {
        methods:{
            changeName(){
                this.passName = 'gettign from method'
            }
        },
        data(){
            return{
                passName:'I am the one',
                age : 23
            };
        },

        components: {
            appUserDetail: UserDetail,
            appUserEdit: UserEdit
        }
    }
</script>

<style scoped>
    div {
        background-color: lightblue;
    }
</style>
