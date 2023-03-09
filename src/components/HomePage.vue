<template>
    <div>
        <h1 v-if="show">Hello from home component is true</h1>
        <h1 v-else>Hello from home component is false</h1>
        <!-- <h2>{{ data }}</h2>
        <h2>{{ msg }}</h2> -->
        <!-- <button v-on:click="hello"  >count method</button> -->
        <button v-on:click="display">Toggle Element</button>


        <h1>This is For Loop</h1>
        <table border="1">
            <tr>
                <td>id</td>
                <td>Name</td>
                <td>Gmail</td>
            </tr>
            <tr  v-for="item in users" :key="item.id">
                <td>{{item.id}}</td>
                <td>{{item.name}}</td>
                <td>{{item.gmail}}</td>
            </tr>
        </table>
    </div>
</template>

<script>
 
 

export default {
    name: 'HomePage',
    props: {
        data: String,
        msg: String,
    },
    // methods:{
    //     hello(){
    //         console.log("this is method");      
    //     }
    // },
    // data() {
    //     return { show: true }
    // },
    methods: {
        display() {
            this.show = !this.show;
        }
    },
    data() {
        return {
            users: [
                {id:1,name:'Aditya',gmail:'aditya@test.com'},
                {id:2,name:'kumar',gmail:'kumar@test.com'},
                {id:3,name:'rom',gmail:'rom@test.com'},
                {id:4,name:'tony',gmail:'tony@test.com'},
            ]
        }
    }
}
</script>