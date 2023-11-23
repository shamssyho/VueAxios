<template>
    <div>
        <h2>Create Post</h2>
        <form @submit.prevent="newPost">
            <div>
                <label for="userId">Post Id</label>
                <input type="text" id="userId" v-model="formData.userId" />
            </div>
            <div>
                <label for="title">Title</label>
                <input type="text" id="title" v-model="formData.title" />
            </div>
            <div>
                <label for="body">Body</label>
                <input type="text" id="body" v-model="formData.body" />
            </div>
            <button>Create post</button>
        </form>
    </div>
</template>

<script>
import axios from "axios"
export default {
    name: "CreatePost",
    data() {
        return {
            formData : {
                userId :"",
                title : "",
                body : "",

            }
        }
    },
    methods: {
        newPost() {
            axios.post("https://jsonplaceholder.typicode.com/posts", this.formData)
                .then((response) => {console.log(response)})
                .catch((error) =>{console.log(error)})

        }
    }
}
</script>

<style></style>