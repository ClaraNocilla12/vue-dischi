<template>
  <div>
    <HeaderPartial />

    <DiscPartial />
  </div>
</template>

<script>
import HeaderPartial from "./partials/HeaderPartial.vue";
import DiscPartial from "./partials/DiscPartial.vue";

export default {
  name: "HomePage",
  components: {
    HeaderPartial,
    DiscPartial,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
// .container-home{
//   height: 100vh;
//   background-color: rgb(58, 69, 87);
// }
</style>
