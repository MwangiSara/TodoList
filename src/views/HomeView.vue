<template>
  <div class="home">
<div class="card shadow" style="background-color: hsla(271, 28%, 54%, 0.702); border: none;">
  <ViewLists />
</div>
  </div>
</template>

<script>
// @ is an alias to /src
import AddList from '@/components/AddList.vue'
import ViewLists from '@/components/ViewLists.vue'


export default {
  name: 'HomeView',
  components: { AddList, ViewLists }
}
</script>

<style >
body{
  background-image: url('../assets/background.jpg');
  background-size: cover; /* Resize the background image to cover the entire container */
  height: 500px; /* You must set a specified height */
  background-position: center; /* Center the image */
  background-repeat: no-repeat; /* Do not repeat the image */

}
.card{
  
  margin: 100px 200px;
  padding: 20px;

}

</style>
