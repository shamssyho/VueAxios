<template>
    <div>
        <h2>Post list</h2>
        <button @click="getPosts">Load Posts</button>
        <div v-for="post in posts" :key="post.id">
            <h3 v-if="errorMsg">{{ errorMsg }}</h3>
            <h3> {{ post.id }} {{ post.title }} </h3>
            <p> {{ post.body }} </p>
            <hr />
        </div>
    </div>
</template>

<script>
import axios from "axios"
export default {
    name: "PostList",
    created(){
        this.getPosts()
    },
    data(){
        return {
            posts : [],
            errorMsg : "",
        }
    },
    methods :{
        getPosts(){
            /* HTTP request */
            axios
            .get("https://jsonplaceholder.typicode.com/posts")
            .then((response)=>{
                this.posts = response.data
            })
            .catch((error)=>{
                console.log(error);
                this.errorMsg = 'Problem to find data'
            })

        }
    }

}
</script>

<style></style>