<template>
    <form action="">
        <h2>Add Friend</h2>
        <input v-model="firstname" type="text" placeholder="First Name" class="form-control">
        <input v-model="lastname" type="text" placeholder="Last Name" class="form-control">
        <input v-model="comment" type="text" placeholder="Comment" class="form-control">
        <button @click="addUser" class="form-control btn" type="submit">ADD</button>
    </form>
</template>

<script>
import axios from 'axios'
export default {
    data() {
        return {
            firstname: '',
            lastname: '',
            comment: '',
        }
    },
    methods: {
        addUser() {
            let user = {
                firstname: this.firstname,
                lastname: this.lastname,
                comment: this.comment,
            }
            axios.post('http://127.0.0.1:81/api/people', user).then(res => {
                console.log(res.data);
            })
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    form {
        width: 40%;
        padding: 20px;
        border-radius: 10px;
        margin: auto;
        margin-top: 20px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
        text-align: center;

    }
    .form-control {
        width: 100%;
        box-sizing: border-box;
        padding: 10px;
        margin-bottom: 16px;
        border: solid 1px rgb(124, 117, 117);
        border-radius: 5px;
        outline: none;
    }
    .btn {
        background: rgb(156, 139, 139);
        border: none;
        color: #fff;
    }
    .btn:hover {
        background: rgb(176, 33, 33);
    }
    h2 {
        margin-bottom: 10px;
    }
</style>
