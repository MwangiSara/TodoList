<template>
    <div class="lists">
        <h1 class="text-">Tasks</h1>
        <div v-if="tasks.length">
            <div v-for="task in tasks" :key="task.id">
                <h2>{{ task.task }}</h2>
            </div>
        </div>
    </div>

</template>

<script>
export default {
data(){
    return{
        tasks:[]
    }
},
// fetching data from the json-server
mounted(){
  fetch('http://localhost:3000/tasks') 
  //the code uses the fetch API to make an HTTP GET request to the URL http://localhost:3000/tasks
    .then(resource => resource.json())
    //The .then method is used to handle the successful response from the fetch request. The first .then function takes the response object (resource) as an argument. Inside this function, the resource.json() method is called to convert the response body into a JavaScript object
    .then(data => this.tasks = data)
    //The second .then method takes the parsed JSON data (data) as an argument.
    .catch(error => console.log(error.message))
    //The .catch method is used to handle any errors that might occur during the fetch operation. It takes an error object (error) as an argument. Inside the .catch function, the code logs the error message (error.message) to the console for debugging purposes.
}
}
</script>

<style>

</style>