<template>
  <div class="container  d-flex justify-content-around align-items-center">
    <div
      class="row row-cols-6 w-75 mt-3 d-flex justify-content-around "
    >
      <!-- <div  v-for="(element, index) in discs" :key="index">
          <img :src="element.poster" alt="">
          <h3 class="text-white">{{element.title}}</h3>
          <h4>{{element.author}}</h4>
          <h4>{{element.year}}</h4>
         
      </div> -->

      <div class="bg-cards row row-cols text-center my-2 mx-1 d-flex justify-content-center flex-wrap p-1" v-for="(element, index) in discs" :key="index">
         <img class="my-2" :src="element.poster" alt="">
          <h5 class="text-white">{{element.title}}</h5>
          <span class="text-secondary">{{element.author}}</span>
          <span class="text-secondary">{{element.year}}</span>
        </div>
      </div>
    </div>
  
</template>

<script>
import axios from "axios";

export default {
  name: "DiscPartial",
  data() {
    return {
      discs: [],
    };
  },

  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        console.log(res.data.response);
        this.discs = res.data.response;
      });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .bg-cards{
        background-color: rgba(0, 0, 0, 0.171);
    }

</style>