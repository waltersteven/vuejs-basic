<template>
    <div class="test">
        <input type="text" v-model="title"><br/>
        <h1>{{title}}</h1>
        <p v-if="showName">{{user.first_name}}</p>
        <p v-else>Nobody</p>
        <!-- <p v-text="user.first_name"></p> -->
        <ul>
            <li v-for="item in items">{{item.title}}</li>
        </ul>
        <button v-on:click="greet('Hello world')">Hey bro</button>
        <br />
        <input type="text" v-on:keyup="pressKey" v-on:keyup.enter="enterHit">
        <hr />
        <label>First name: </label><input type="text" v-model="user.first_name">
        <br />
        <label>Last name: </label><input type="text" v-model="user.last_name">
        <h3>{{fullname}}</h3>
        <h2>{{msg}}</h2>
    </div>
</template>

<script>
export default {
    name: 'prueba',
    props: {
        msg: {
            type: String,
            default: 'Foobar'
        }
    },
    data() {
        return {
            title: 'Hello world',
            user: {
                first_name: 'Walter',
                last_name:  'Pariona'
            },
            showName: true,
            items: [
                {title: 'Item one'},
                {title: 'Item two'},
                {title: 'Item three'}                
            ]
        }
    },
    methods: {
        greet: function(greeting){
            alert("what up "+ greeting);
        },
        pressKey: function(e){
            console.log(e.target.value);
        },
        enterHit: function(e){
            console.log("you hit enter");
        }
    },
    computed: {
        fullname: function(){
            return this.user.first_name + ' ' + this.user.last_name;
        }
    }
}
</script>

<style scoped>

</style>


