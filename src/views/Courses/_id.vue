<script>
import {onMounted, } from 'vue'
import { useRoute } from 'vue-router'
import axios from 'axios'
export default {
  setup() {
    const route = useRoute()
    onMounted(() => {
      console.log(route);
      console.log(route.params.id);

      axios
      .get('https://vue-lessons-api.herokuapp.com/courses/${route.params.id}')
      .then((res) =>{
        console.log(res);
      })
    })
    return {};
  },
};
</script>
<template>
  <div>
    <div>
      <h1></h1>
      <h2>NTD:</h2>
      <img src="" alt="" />
      <div>
        <img src="" alt="" />
        <p></p>
      </div>
    </div>
    <!-- error_message -->
    <h1></h1>
  </div>
</template>

<style></style>
